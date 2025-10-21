# Clustering Multidimensional Time Series — Modeling Human Behavior

Clustering is a general technique for discovering patterns in datasets in an exploratory way. In many cases, especially in the social sciences, the data we analyze take the form of time series — repeated interactions that unfold over time. These sequences are often multidimensional: what someone does is shaped by what they experience, and both evolve together. Social science experiments, particularly those inspired by game theory, frequently produce exactly this kind of data. That makes clustering not only a universal tool to master, but also one with direct applications for understanding human and agent behavior in multidimensional settings.

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

- [Dal Bó & Fréchette (2018)](https://www.jstor.org/stable/pdf/26417201)  
  - 103 sessions, 1,734 subjects, 116,644 observations  
- [Bigoni et al. (2024)](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4809158)  
  - 27 sessions, 598 subjects, 60,334 observations  
- [Embrey et al. (2018)](https://academic.oup.com/qje/article/133/1/509/4095199)  
  - 27 sessions, 552 subjects, 65,720 observations  
- [Mazur et al. (2025)](https://github.com/lechmazur/pgg_bench)  


---
## Readings

- Von Luxburg U, Williamson RC, Guyon I. Clustering: Science or art?. (2012) [Link](https://proceedings.mlr.press/v27/luxburg12a/luxburg12a.pdf)
- Halkidi, M., Batistakis, Y. and Vazirgiannis, M., 2001. On clustering validation techniques. [Link](https://web.itu.edu.tr/sgunduz/courses/verimaden/paper/validity_survey.pdf)
