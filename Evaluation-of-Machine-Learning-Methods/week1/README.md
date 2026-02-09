Exercise1: Comparing cross-validation methods for data with non-independent datapoints (replicates)

Cross-Validation Strategies

Leave-One-Out Cross-Validation (LOOCV)
  Leaves out one observation at a time
  Invalid for replicated data
  Leads to information leakage because replicates of the same mixture appear in both training and test sets

Leave-Replicas-Out Cross-Validation (LROCV)
  Leaves out all replicates of one mixture at a time
  Ensures independence between training and test data
  Provides a more realistic estimate of generalization performance

Results:
  LOOCV produces inflated c-index values due to replicate leakage
  LROCV consistently yields lower but more realistic performance estimates
  Total concentration (Cd + Pb) often achieves the highest c-index due to variance reduction
  Sensor signals (Mod1–Mod3) generalize well across mixtures
