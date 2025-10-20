# Ethics of Artificial Intelligence

Bias and fairness in machine learning examine how social inequalities and value judgments become embedded in algorithms through data, design, and deployment choices. In this session, we will pay particular attention to how bias can be causally measured — understanding not just where it appears, but why it arises and how to distinguish genuine bias from contextual effects.

---

## 📖 Core Readings

- Caliskan, A., Bryson, J. J., & Narayanan, A. (2017). *Semantics derived automatically from language corpora contain human-like biases* (WEAT). [Link](https://www.science.org/doi/pdf/10.1126/science.aal4230)
- Fiske, S. T., Cuddy, A. J., & Glick, P. (2002). *Stereotype Content Model: Warmth and Competence as universal dimensions of social perception.*  [Link](https://d1wqtxts1xzle7.cloudfront.net/49013872/Warmth_and_Competence_as_Universal_Dimen20160921-3310-1lvtfe0-libre.pdf?1474469807=&response-content-disposition=inline%3B+filename%3DWarmth_and_Competence_as_Universal_Dimen.pdf&Expires=1758630848&Signature=J0~E420wGbv20fSrXaTC6wK7YDSj0jAeACA-ORvHlCNLodr98qOxCrXoOZhikOjGduTj-DRhYUVYqVHJ0cGK~3dVIiMEKlcj~f8fcGKx0s0Nt6GH5afywe-eZs8o~zHhwO4XlwO74UC0ckdwP2dGUj75A7DigQLDZm5my-U8YGba~h-k20BkhdVzZa0kKq9UcpkOGCXcqDqNDoLNEDex1soxu-5dcMJPmfTtGsbqrmlgGUMxScFhsbOmzqfa2v9OdxfQIuV5fg9UYXetyaNhcY-Il6VexdXxmXKhXrfSkJYyVxlZ0MeilZtF4Ar66dfeSUvQQuFCGYP5NiNI85Sw-A__&Key-Pair-Id=APKAJLOHF5GGSLRBV4ZA)
- Bailey, A. H. (2022). *Based on billions of words on the internet, people = men.* Science Advances. [Link](https://www.science.org/doi/full/10.1126/sciadv.abm2463)  
- Bai, X., Wang, A., Sucholutsky, I., & Griffiths, T. L. (2025). *Explicitly unbiased large language models still form biased associations.* [Link](https://doi.org/10.1073/pnas.2416228122)
- Yang, J.C., Dailisan, D., Korecki, M., Hausladen, C.I. and Helbing, D., (2024). *Llm voting: Human choices and ai collective decision-making*. [Link](https://ojs.aaai.org/index.php/AIES/article/view/31758)

### Optional Readings
- Radford, A., Kim, J. W., Hallacy, C., Ramesh, A., Goh, G., Agarwal, S., Sastry, G., Askell, A., Mishkin, P., Clark, J., Krueger, G., & Sutskever, I. (2021). *Learning Transferable Visual Models From Natural Language Supervision* (CLIP). [Link](https://arxiv.org/abs/2103.00020). 
---


## 📘 Lecture Notes

### Introduction
- Bias and fairness in ML explore how social inequalities and value judgments are embedded in algorithms through data, design, and deployment choices.  
- We will pay particular attention to how to causally measure bias — understanding not only where it appears, but why it arises.

#### Applications Where Bias Occurs
- Labour market discrimination (e.g., Lakisha & Jamal paper)
- Predictive policing and "future criminals"
- Netherlands childcare benefits scandal
- Biased advertisement exposure
- COMPAS recidivism prediction system

#### Key Concepts
- The choice of data shapes how ML models define and operationalize concepts.
- Take a sociotechnical perspective — bias stems from both technical and social systems.

#### Discussion Starters
- Autonomous cars and the trolley problem
- Should we open-source language models? (Dual-use dilemma)


### Operationalising Fairness Criteria

#### Legal and Ethical Context
- Fairness principles often originate in legal frameworks.  
  - Example: In Germany, the General Equal Treatment Act defines anti-discrimination laws.

#### Sources of Bias
- Human bias (e.g., in hiring decisions)
- Negative feedback loops (e.g., biased police attention)
- Sample imbalance (minority groups underrepresented)
- Unreliable data (e.g., inaccurate census data in minority neighborhoods)

#### Bias Mitigation Across the ML Pipeline
- Problem definition  
- Data collection  
- Model development (focus of most AI research)  
- Use of predictions in practice  
- Feedback loops and long-term monitoring  

#### Legal Fairness Frameworks
- Disparate treatment: Procedural fairness (intentional discrimination)  
- Disparate impact: Substantive fairness (outcomes regardless of intent)

#### Fairness Criteria and Trade-offs
- Fairness definitions are mutually exclusive; trade-offs are inevitable:
  - Independence
  - Separation
  - Sufficiency


### Biases in Natural Language Processing (NLP)

#### Illustrative Example
- Translation bias:  
  “The doctor called the nurse” → “Der Arzt rief die Krankenschwester” (gender stereotype)

#### Word Embeddings and Representation Bias
- Early models: Bag-of-Words (word counts)
- Modern models: Vector representations (e.g., word2vec, GloVe)
  - Each word represented as a 300-dimensional vector
  - Trained on large text corpora to predict context words
- GloVe (Pennington et al., 2014)  
  - Linear analogies: king - man + woman = queen
- Bias in Word Embeddings:  
  - Encodes social stereotypes present in training data  
  - Reference: https://arxiv.org/abs/1607.06520

#### Why Bias Persists in NLP
- Models trained on human-generated text inherit human prejudices  
- Stereotypes reflected in linguistic patterns  
- Difficult to remove — even for binary gender distinctions  
- Geometric structure of embeddings retains bias  
- Complex, multidimensional stereotypes are hard to define or remove

#### Best Practices
- Examine data and model behavior critically  
- Identify sources of bias  
- Understand and mitigate their impact

### Fairness and Causality

#### Simpson’s Paradox
- Example: Hiring rates differ by department  
- Paradox: A trend seen in groups reverses when data is aggregated  
- Conditioning on certain variables can flip conclusions

#### Causal Inference
- Goal: Understand why bias appears, not just where it appears  
- Reference: Judea Pearl, The Book of Why  
- Confounders: Variables affecting both predictor and outcome (e.g., occupation, pose, dataset source)  
- Learning causal graphs: Helps separate genuine social bias from context-driven differences

---
## 💻 Pratical Part

Implement parts of: Hausladen, C. I., Knott, M., Camerer, C. F., & Perona, P. (2024). *Social perception of faces in a vision-language model.*  [Link](https://dl.acm.org/doi/pdf/10.1145/3715275.3732041)
  
### Core Concepts

- CLIP-Embeddings
- Cosine Similarity
- Social Perception Theories
- Causal Operationalization
- Counterfactual Fairness

---

## 📊 Project Ideas & Datasets

- Explore new LLMs such as **DeepSeek** or **ApertusAI (Swiss)** for bias analysis.
- Hiring Discrimination by Agentic AI (e.g. LinkedIn's new [Hiring Assistant](https://business.linkedin.com/talent-solutions/hiring-assistant?trk=leader)

---
## Reference
This lecture was insipred by [CS 281 - Spring 2025](https://stanfordaiethics.github.io/syllabus.html).

