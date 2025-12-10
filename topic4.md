# Clustering Multidimensional Time Series — Modeling Human Behavior

Clustering is a general technique for discovering patterns in datasets in an exploratory way. In many cases, especially in the social sciences, the data we analyze take the form of time series — repeated interactions that unfold over time. These sequences are often multidimensional: what someone does is shaped by what they experience, and both evolve together. Social science experiments, particularly those inspired by game theory, frequently produce exactly this kind of data. That makes clustering not only a universal tool to master, but also one with direct applications for understanding human and agent behavior in multidimensional settings.

---

## 📖 Readings

- von Luxburg, U., Williamson, R. C., & Guyon, I. (2012).  
  *Clustering: Science or art?*  
  Proceedings of ICML Workshop on Unsupervised and Transfer Learning, JMLR: Workshop and Conference Proceedings, 27, 65–79.  
  [Link](https://proceedings.mlr.press/v27/luxburg12a/luxburg12a.pdf) 🎧 ~16:22 min (1.5× estimated listening time)

- Hennig, C. (2015).  
  *What are the true clusters?*  
  Pattern Recognition Letters, 64, 53–62.  
  [Link](https://doi.org/10.1016/j.patrec.2015.04.009) 🎧 ~26:44 min (1.5× estimated listening time)

- Montero-Porras, E., Grujić, J., Domingos, E. F., & Lenaerts, T. (2022).  
  *Inferring strategies from observations in long iterated prisoner’s dilemma experiments.*  
  Scientific Reports, 12, 7589.  
  [Link](https://doi.org/10.1038/s41598-022-11654-2) 🎧 ~27:56 min (1.5× estimated listening time)



### Optional 

- Petitjean, F., Ketterlin, A., & Gançarski, P. (2011).  
  *A global averaging method for dynamic time warping, with applications to clustering.*  
  Pattern Recognition, 44(3), 678–693.  
  [Link](https://doi.org/10.1016/j.patcog.2010.09.013) 🎧 ~52:31 min (1.5× estimated listening time)
- Gerlach et al. (2018) — [Link](https://doi.org/10.1038/s41562-018-0419-z)  
- Halkidi et al. (2001) — [Link](https://web.itu.edu.tr/sgunduz/courses/verimaden/paper/validity_survey.pdf)  
- Wang (2025) — [Link](https://doi.org/10.1007/s11403-025-00451-5)

---

## 🔑 Core Concepts


1. **Multidimensional Dynamic Time Warping (DTW)**  
   - Aligns sequences that may be out of phase.  
   - Uses cost matrices & warping paths to compute similarity.  
   - Compares multi-channel data (e.g. trajectories, multi-modal behavior).  
   - Trade-off between dependent vs. independent warping.  

4. **Clustering Methods**  
   - **Hierarchical clustering**: builds dendrograms, sensitive to linkage choices.  
   - **PAM (Partitioning Around Medoids)**: medoid-based, robust for DTW distances.  
   - **DBSCAN/HDBSCAN**: density-based, identifies irregularities & outliers.  

5. **Evaluation & Validation**  
   - Internal indices (silhouette, Dunn, Davies–Bouldin).  
   - External validation (ground-truth labels, if available).  
   - Cluster stability: bootstrap, resampling.  
   - Visualization: distance matrices, dendrograms.  

---

## 📖 Datasets

### EU Parliament Voting

Research idea: Treat European Parliament voting behavior as a high-dimensional time series and cluster MEPs based on evolving cooperation and conflict. Explore whether political alliances change over time and by issue area.

- Data: [https://github.com/HowTheyVote/data](https://github.com/HowTheyVote/data)
- Related paper: Rosalino, S. M., Curado, A., & Pinheiro, F. L. (2025). *Multi-polarization during the 9th European Parliament.* arXiv:2507.03214 [physics.soc-ph].  
  [https://arxiv.org/abs/2507.03214](https://arxiv.org/abs/2507.03214)


### On Standard Cooperation Games

- [Dal Bó & Fréchette (2018)](https://www.jstor.org/stable/pdf/26417201)  
  - 103 sessions, 1,734 subjects, 116,644 observations  
- [Bigoni et al. (2024)](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4809158)  
  - 27 sessions, 598 subjects, 60,334 observations  
- [Embrey et al. (2018)](https://academic.oup.com/qje/article/133/1/509/4095199)  
  - 27 sessions, 552 subjects, 65,720 observations  
- [Mazur et al. (2025)](https://github.com/lechmazur/pgg_bench)  

