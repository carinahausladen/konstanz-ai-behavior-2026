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

## 📖 Dataset

- **Dal Bó & Fréchette (2018)** — Indefinite Repeated Games with Perfect Monitoring  
  [JSTOR link](https://www.jstor.org/stable/pdf/26417201)  
  - 103 sessions, 1,734 subjects, 116,644 observations  

- **Bigoni et al. 2024 (Indefinite Imperfect Monitoring)**  
  [SSRN link](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4809158)  
  - 27 sessions, 598 subjects, 60,334 observations  

- **Embrey et al. (2018)** — Finite Repeated Games with Perfect Monitoring  
  [Quarterly Journal of Economics](https://academic.oup.com/qje/article/133/1/509/4095199)  
  - 27 sessions, 552 subjects, 65,720 observations  

- **Mazur et al. (2025)** — *PGG-Bench: Benchmarking Public Goods Games with LLMs*  
  [GitHub repository](https://github.com/lechmazur/pgg_bench)  
