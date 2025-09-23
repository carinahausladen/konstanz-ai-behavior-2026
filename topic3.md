# Social Choice for LLM Alignment

---

Social choice theory studies how individual preferences can be aggregated into a collective decision.  
For computer scientists, it offers mathematical tools for preference aggregation.  
For social scientists, it provides frameworks for fairness, representation, and legitimacy.  

In the context of LLM alignment, these two worlds meet: we want models to reflect diverse human values, but human feedback is fragmented, subjective, and culturally varied.  
Proportional aggregation methods — drawn from voting theory — may help us avoid majority domination while preserving minority perspectives in RLHF pipelines.  

---

## 🔑 Core Concepts

1. **Social Choice Theory**
   - Framework for aggregating individual preferences into collective outcomes.  
   - Classic voting rules: majority, Borda, Condorcet.  
   - Arrow’s theorem: impossibility of a perfect rule.  

2. **Proportional Aggregation**
   - Representation proportional to group size/preferences.  
   - Examples: Proportional Approval Voting, Single Transferable Vote (STV), Thiele methods.  
   - Trade-offs: proportionality vs. efficiency.  

3. **RLHF (Reinforcement Learning from Human Feedback)**
   - Pipeline: pretraining → supervised fine-tuning → RLHF with preference models.  
   - Aggregation enters when building preference models from human judgments.  

4. **Fairness & Representation**
   - Majority rule risks marginalizing minority views.  
   - Proportional aggregation offers a way to preserve value pluralism in AI alignment.  

---
## 📖 Readings

### Core
1. Kirk, H. R., Whitefield, A., Röttger, P., Bean, A., Margatina, K., Mosquera, R., Bartolo, M., Williams, A., He, H., Vidgen, B., & Hale, S. A. (2024).  
   *The PRISM Alignment Dataset: What Participatory, Representative and Individualised Human Feedback Reveals about the Subjective and Multicultural Alignment of Large Language Models.* arXiv.  
   [arXiv link](https://arxiv.org/abs/2404.16019)  

2. Brandt, F., Conitzer, V., Endriss, U., Lang, J., & Procaccia, A. D. (2016).  
   *Handbook of Computational Social Choice.* Springer.  
   [SpringerLink](https://link.springer.com/chapter/10.1007/978-3-642-02839-7_6)  

### Optional
1. Sen, A. K. (1970). *Collective Choice and Social Welfare.* Holden-Day, San Francisco.  
   [Harvard University Press Link](https://www.hup.harvard.edu/books/9780674919211)  

2. Christiano, P., Leike, J., Brown, T. B., Martic, M., Legg, S., & Amodei, D. (2017).  
   *Deep Reinforcement Learning from Human Preferences.* NeurIPS 2017.  
   [arXiv](https://arxiv.org/abs/1706.03741)  


