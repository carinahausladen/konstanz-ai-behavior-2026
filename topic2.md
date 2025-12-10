# Modeling Social Dilemmas through Reinforcement Learning

This lecture explores how social dilemma games help us understand cooperation and conflict in human decision-making. 
We connect ideas from behavioral economics and machine learning to study how people adapt their strategies over time. Reinforcement learning (RL) provides a framework for modeling these adaptive behaviors, while inverse reinforcement learning (IRL) helps infer the motivations behind observed choices.

---
## 📖 Readings

- Köster, R., O’Reilly, J. X., Yeung, N., Strouse, D., Phillips, L., Chadwick, M., … & Banerjee, S. (2025).  
  *Deep reinforcement learning can promote sustainable human behaviour in a common-pool resource problem.*  
  Nature Communications, 16, 980.  
  [Link](https://doi.org/10.1038/s41467-025-58043-7)

- Tacchetti, A., Köster, R., Balaguer, J., … & Summerfield, C. (2024).  
  *Deep mechanism design: Learning social and economic policies for human benefit.*  
  Proceedings of the National Academy of Sciences.  
  [Link](https://www.pnas.org/doi/10.1073/pnas.2319949121)

- Dolgopolov, A. (2024).  
  *Reinforcement learning in a prisoner’s dilemma.*  
  Games and Economic Behavior, 144, 84–103.  
  [Link](https://doi.org/10.1016/j.geb.2024.01.004)

- Leibo, J. Z., Zambaldi, V., Lanctot, M., Marecki, J., & Graepel, T. (2017).  
  *Multi-agent reinforcement learning in sequential social dilemmas.*  
  arXiv preprint.  
  [Link](https://arxiv.org/abs/1702.03037)


### Optional 

- Camerer & Ho (1999) — [Link](https://doi.org/10.1111/1468-0262.00054)  
- Peysakhovich & Lerer (2017) — [Link](https://arxiv.org/abs/1709.02865)  
- Zheng et al. (2024) — [Link](https://doi.org/10.1016/j.chaos.2024.115568)  
- Foerster et al. (2018) — [Link](https://arxiv.org/abs/1709.04326)



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


