# Modeling Social Dilemmas through Reinforcement Learning

This lecture explores how social dilemma games help us understand cooperation and conflict in human decision-making. 
We connect ideas from behavioral economics and machine learning to study how people adapt their strategies over time. Reinforcement learning (RL) provides a framework for modeling these adaptive behaviors, while inverse reinforcement learning (IRL) helps infer the motivations behind observed choices.

---

## 📖 Readings

- Köster, R., O’Reilly, J. X., Yeung, N., Strouse, D., Phillips, L., Chadwick, M., … & Banerjee, S. (2025).  
  *Deep reinforcement learning can promote sustainable human behaviour in a common-pool resource problem.*  
  **Nature Communications, 16, 980.**  
  [https://doi.org/10.1038/s41467-025-58043-7](https://doi.org/10.1038/s41467-025-58043-7)  

- Tacchetti, A., Koster, R., Balaguer, J., … & Summerfield, C. (2024).  
  *Deep mechanism design: Learning social and economic policies for human benefit.*  
  **Proceedings of the National Academy of Sciences (PNAS).**  
  [https://www.pnas.org/doi/10.1073/pnas.2319949121](https://www.pnas.org/doi/10.1073/pnas.2319949121)

- Dolgopolov, A. (2024).
  *Reinforcement learning in a prisoner’s dilemma.*
  **Games and Economic Behavior**, 144, 84–103.  
  [https://doi.org/10.1016/j.geb.2024.01.004](https://doi.org/10.1016/j.geb.2024.01.004)

- Zheng, G., Zhang, J., Deng, S., Cai, W., & Chen, L. (2024).
  *Evolution of cooperation in the public goods game with Q-learning.*
  **Chaos, Solitons & Fractals**, 188, 115568.  
  [https://doi.org/10.1016/j.chaos.2024.115568](https://doi.org/10.1016/j.chaos.2024.115568)

### Optional

- Erev, I., & Roth, A. E. (1998).
  *Predicting How People Play Games: Reinforcement Learning in Experimental Games with Unique, Mixed Strategy Equilibria.*
  **American Economic Review**, 88(4), 848–881.  
  [https://economics.ucsd.edu/~jandreon/Econ264/papers/Erev%20Roth%20AER%201998.pdf](https://economics.ucsd.edu/~jandreon/Econ264/papers/Erev%20Roth%20AER%201998.pdf)

---
## 📘 Lecture Notes

- Social Dilemma Games
   - Situations with conflict between individual and collective interest.  
   - Examples: Prisoner’s Dilemma, Stag Hunt, Public Goods Game.  
   - Cooperation vs. defection as emergent dynamics.
- Reinforcement Learning (RL)
   - Agents learn from rewards and punishments over time.  
   - Focus on adaptation rather than fixed rational strategies.
- Markov Decision Processes (MDPs)
   - Formalism for sequential decision-making under uncertainty.  
   - States, actions, transitions, rewards.  
   - Provides the backbone for repeated social dilemma modeling.
- Q-Learning
   - Core algorithm of RL.  
   - Learns state–action values through trial and error.  
   - Simple but powerful: applies to small matrix games and large-scale AI systems.
- Inverse Reinforcement Learning (IRL)
   - From observed choices, infer the hidden reward function.  
   - Useful in social science: recover fairness concerns, reciprocity, inequality aversion.  


