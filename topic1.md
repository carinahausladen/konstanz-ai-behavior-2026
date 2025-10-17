# Bias and Fairness in LLMs / VLMs

Large language and vision–language models are increasingly used in settings where their outputs can reflect and amplify human stereotypes. Studying bias in these models is interesting because it connects technical tools like embeddings and cosine similarity with psychological theories of social perception such as warmth and competence. This topic helps us see how abstract vectors in embedding space can reveal patterns of unfairness, and how operationalizing social science theories in AI evaluation offers a bridge between human-centered concerns and machine learning methods.


---

## 🔑 Core Concepts

1. **CLIP (Contrastive Language–Image Pretraining)**
   - Dual encoders, joint embedding space, contrastive learning.

2. **Embeddings**
   - Vectors as compressed meaning.
   - Intuition: “semantic geography.”

3. **Cosine Similarity**
   - Geometric intuition → direction matters, not length.

4. **Social Perception Theories**
   - Psychological dimensions: warmth, competence, agency, etc.

5. **Operationalization**
   - Turning theory into vectors.
   - Causally Measuring alignment between text (theory) and images (model outputs).

---

## 📖 Core Readings

- Radford, A., Kim, J. W., Hallacy, C., Ramesh, A., Goh, G., Agarwal, S., Sastry, G., Askell, A., Mishkin, P., Clark, J., Krueger, G., & Sutskever, I. (2021). *Learning Transferable Visual Models From Natural Language Supervision* (CLIP). [Link](https://arxiv.org/abs/2103.00020). 
- Caliskan, A., Bryson, J. J., & Narayanan, A. (2017). *Semantics derived automatically from language corpora contain human-like biases* (WEAT). [Link](https://www.science.org/doi/pdf/10.1126/science.aal4230)
- Hausladen, C. I., Knott, M., Camerer, C. F., & Perona, P. (2024). *Social perception of faces in a vision-language model.*  [Link](https://dl.acm.org/doi/pdf/10.1145/3715275.3732041)
- Fiske, S. T., Cuddy, A. J., & Glick, P. (2002). *Stereotype Content Model: Warmth and Competence as universal dimensions of social perception.*  [Link](https://d1wqtxts1xzle7.cloudfront.net/49013872/Warmth_and_Competence_as_Universal_Dimen20160921-3310-1lvtfe0-libre.pdf?1474469807=&response-content-disposition=inline%3B+filename%3DWarmth_and_Competence_as_Universal_Dimen.pdf&Expires=1758630848&Signature=J0~E420wGbv20fSrXaTC6wK7YDSj0jAeACA-ORvHlCNLodr98qOxCrXoOZhikOjGduTj-DRhYUVYqVHJ0cGK~3dVIiMEKlcj~f8fcGKx0s0Nt6GH5afywe-eZs8o~zHhwO4XlwO74UC0ckdwP2dGUj75A7DigQLDZm5my-U8YGba~h-k20BkhdVzZa0kKq9UcpkOGCXcqDqNDoLNEDex1soxu-5dcMJPmfTtGsbqrmlgGUMxScFhsbOmzqfa2v9OdxfQIuV5fg9UYXetyaNhcY-Il6VexdXxmXKhXrfSkJYyVxlZ0MeilZtF4Ar66dfeSUvQQuFCGYP5NiNI85Sw-A__&Key-Pair-Id=APKAJLOHF5GGSLRBV4ZA)
- Bailey, A. H. (2022). *Based on billions of words on the internet, people = men.* Science Advances. [Link](https://www.science.org/doi/full/10.1126/sciadv.abm2463)  
- Bai, X., Wang, A., Sucholutsky, I., & Griffiths, T. L. (2025). *Explicitly unbiased large language models still form biased associations.* [Link](https://doi.org/10.1073/pnas.2416228122)
- Yang, J.C., Dailisan, D., Korecki, M., Hausladen, C.I. and Helbing, D., (2024). *Llm voting: Human choices and ai collective decision-making*. [Link](https://ojs.aaai.org/index.php/AIES/article/view/31758

---

## 📊 Project Ideas & Datasets

- Explore new LLMs such as **DeepSeek** or **ApertusAI (Swiss)** for bias analysis.  

---

## 🎓 Tutorials & Resources

- [Primer on LLM Embeddings — Hugging Face](https://huggingface.co/spaces/hesamation/primer-llm-embedding?section=what_are_embeddings)  
