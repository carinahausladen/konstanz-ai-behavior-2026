# Ethics of Artificial Intelligence

Bias and fairness in machine learning examine how social inequalities and value judgments become embedded in algorithms through data, design, and deployment choices. In this session, we will pay particular attention to how bias can be causally measured — understanding not just where it appears, but why it arises and how to distinguish genuine bias from contextual effects.

---

## 📖 Readings

- Gallegos, I. O., Rossi, R. A., Barrow, J., Tanjim, M. M., Kim, S., Dernoncourt, F., Yu, T., Zhang, R., & Ahmed, N. K. (2024).  
  *Bias and fairness in large language models: A survey.*  
  Computational Linguistics, 50(3), 1097–1179.  
  [Link](https://doi.org/10.1162/coli_a_00524) 🎧 ~1:12:48 min (1.5× estimated listening time)

- Bailey, A. H. (2022).  
  *Based on billions of words on the internet, people = men.*  
  Science Advances.  
  [Link](https://www.science.org/doi/full/10.1126/sciadv.abm2463) 🎧 ~32:10 min (1.5× estimated listening time)

- Bai, X., Wang, A., Sucholutsky, I., & Griffiths, T. L. (2025).  
  *Explicitly unbiased large language models still form biased associations.*  
  Proceedings of the National Academy of Sciences.  
  [Link](https://doi.org/10.1073/pnas.2416228122) 🎧 ~20:40 min (1.5× estimated listening time)

- Khan, F. A., Sivakumar, N., Wang, Y. O., Metcalf, K., Camacho, C., & Theobald, B.-J. (2025).  
  *Investigating intersectional bias in large language models using confidence disparities in coreference resolution.*  
  Proceedings of COLM 2025.  
  [Link](https://arxiv.org/abs/2508.07111) 🎧 ~42:00 min (1.5× estimated listening time)


---

## 📘 Lecture Notes

### Algorithmic Bias: Real Systems Harm Real People

Ethics of AI has several aspects, and there are many examples to be named. One particularly impactful example is hiring discrimination, which has deep roots in economic research.

The literature on hiring discrimination in economics has developed over decades, particularly through **correspondence studies**. The seminal work by [Bertrand and Mullainathan (2004)](https://www.aeaweb.org/articles?id=10.1257/0002828042002561) pioneered a causal approach to measuring hiring discrimination. Their methodology involved sending matched CVs to companies, varying only one characteristic that could be the basis of discrimination—such as age, gender, or race.

Their groundbreaking finding revealed systematic discrimination: 

> Resumes with White-sounding names (like "Emily" and "Greg") received 50% more callbacks than identical resumes with Black-sounding names (like "Lakisha" and "Jamal").

Similar patterns of bias have now been documented in AI systems. A [2024 Bloomberg investigation](https://www.bloomberg.com/graphics/2024-openai-gpt-hiring-racial-discrimination/) demonstrated that OpenAI's GPT-3.5 exhibits systematic bias in resume ranking based solely on names. When asked to rank identical resumes 1,000 times, GPT showed preference patterns that would fail anti-discrimination benchmarks used to assess job discrimination against protected groups.
A notable legal case involved age discrimination in AI hiring systems. In [*Mobley v. Workday*](https://edition.cnn.com/2025/05/22/tech/workday-ai-hiring-discrimination-lawsuit), the AI company faced allegations that its hiring assistance system discriminated against older candidates, and prevented people over 40 from getting hired.
More recently, [LinkedIn launched a hiring assistant](https://business.linkedin.com/hire/hiring-assistant?ss=1) that goes beyond simple CV processing. **Agentic system** not only processes CVs but also analyzes multiple aspects of candidates, writes correspondence to candidates, and manages various stages of the hiring pipeline. 

### Defining Bias for LLMs

In the next part of the lecture, we explore what bias actually means in the context of Large Language Models and develop the conceptual tools to identify and measure bias in AI systems.

#### Fairness Definitions: Two Competing Visions

In the Workday discrimination case, age was the **protected attribute**—a characteristic that should not form the basis for discriminatory treatment. These typically include age, race, gender, religion, disability status, and national origin.

But identifying what to protect is only the first step. The harder question is: *how* do we ensure fair treatment?
**Group Fairness** advocates argue that all demographic groups should have equal success rates. If 50% of 25-year-olds get hired, then 50% of 55-year-olds should too. This perspective prioritizes equal outcomes across groups.
**Individual Fairness** advocates argue that people with similar qualifications should be treated similarly, regardless of demographics. Someone aged 25 and someone aged 55 with identical skills should receive identical treatment.

These two visions can conflict. A hiring system might achieve group fairness (equal rates across age groups) while failing individual fairness (treating similar candidates differently based on age), or vice versa. **There is no universal right answer.** As citizens, we should actively engage in domain-specific deliberation and make informed collective decisions about which principle to prioritize.


### The LLM Life-Cycle: Three Entry Points for Bias

An interesting example comes from the [**PULSE Controversy**](https://twitter.com/chicken3gg/status/1274314622447820801). PULSE was designed to enhance low-resolution images into high-resolution ones. The problem? When given pixelated images of Black individuals (e.g. Barack Obama), it systematically generated high-resolution images of White faces.

The controversy sparked a heated debate on Twitter among AI researchers: *Where exactly did this bias enter the system?*

[Yann LeCun argued](https://twitter.com/ylecun/status/1274782757907030016) it came from the **training data**: PULSE was pre-trained on Flickr-Faces-HQ, a dataset that predominantly contains images of White people. 

> If your training set is biased, your model will be biased.

Others countered it was **model optimization**: 

> The L2 loss function (minimizing average error) makes everyone look White. If they had used L1 loss (minimizing median error) instead, everyone would look Black. The choice of objective function directly shaped the bias.

Still others pointed to **evaluation**: 

> As long as progress is benchmarked on biased data, models will reflect those biases. Without fairness metrics in evaluation, engineers have no signal that something is wrong.
The uncomfortable truth? **All of the above.** Bias compounds across multiple stages of the ML pipeline.


### Five Fairness Desiderata


How do we operationalize fairness in large language models? Fairness is not a single switch we can turn on. It is a family of competing desiderata:


##### 1) Fairness Through Unawareness

A tempting idea is: *just remove protected attributes from the input.* If the model never sees race or gender (or anything that explicitly signals them), it cannot discriminate — right?
The problem is that this rarely works in practice. Models can pick up **proxy variables** (names, neighborhoods, jobs, writing style, etc.) that correlate with protected attributes. So [“blindness” can still reproduce biased behavior](https://dl.acm.org/doi/full/10.1145/3757887.3763007), just less transparently.

##### 2) Invariance

Invariance requires that model outputs remain stable when protected attributes are swapped **while everything else is held constant**.
This mirrors the logic of correspondence studies swap one attribute, see whether outcomes shift.
How to measure invariance reliably is still an active research area. Recently, [Anthropic suggested](https://alignment.anthropic.com/2026/hot-mess-of-ai/) measuring “incoherence” via a bias–variance decomposition of model error.

##### 3) Equal Social Group Associations

This desideratum targets *associations* in model outputs: neutral attributes (e.g., “intelligent,” “competent,” “leader”) should not be disproportionately linked to one social group over another.
Why care? Because humans often carry implicit race–status associations (RSAs) that link some groups with higher status than others — and these [associations predict downstream judgments](https://psycnet.apa.org/manuscript/2020-66288-001.pdf).

##### 4) Equal Neutral Associations

Under this principle, protected attribute terms (e.g., “he” vs. “she”) should appear with equal likelihood **in neutral contexts**.
In other words: when the prompt does not contain group-relevant information, the model should not systematically default to one group term over another. 

##### 5) Replicated Distributions

This approach demands that model outputs mirror **reference dataset distributions** for neutral elements across groups, preventing the invention of new disparities.

---

## 📊 Project Ideas & Datasets

- Explore new LLMs such as **DeepSeek** or **ApertusAI (Swiss)** for bias analysis.
- Hiring Discrimination by Agentic AI (e.g. LinkedIn's new [Hiring Assistant](https://business.linkedin.com/talent-solutions/hiring-assistant?trk=leader)

---

## 📚 References

[^1]: Bertrand, M., & Mullainathan, S. (2004). Are Emily and Greg More Employable than Lakisha and Jamal? A Field Experiment on Labor Market Discrimination. *American Economic Review*, 94(4), 991-1013. https://doi.org/10.1257/0002828042002561

[^2]: Yin, L., Alba, D., & Nicoletti, L. (2024, March 8). OpenAI's GPT Is a Recruiter's Dream Tool. Tests Show There's Racial Bias. *Bloomberg*. https://www.bloomberg.com/graphics/2024-openai-gpt-hiring-racial-discrimination/

An interesting related lecture: [CS 281 - Spring 2025](https://stanfordaiethics.github.io/syllabus.html).

