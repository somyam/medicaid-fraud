Medicaid program integrity faces a persistent detection problem: fraudulent billing patterns are 
heterogeneous, evolve faster than rule-based detection systems, and typically surface only after 
years of financial exposure. This paper describes a two-stage provider-level fraud detection 
pipeline built on the CMS Medicaid Provider Claims Dataset, covering 162 million claim-month 
aggregates from 1.42 million individual providers across 2018–2024. The first stage computes 
peer-normalized robust z-scores across three independent fraud-relevant signals—unit price 
(paid per claim), billing volume, and billing intensity (claims per beneficiary)—with peer groups 
defined by taxonomy, state, and procedure code. The second stage trains a feed-forward 
autoencoder on aggregated provider-year features to identify multivariate anomalies that 
single-signal thresholds miss. The two methods produce ranked candidate lists with 22% 
overlap at top-100, confirming that threshold-based and reconstruction-based approaches 
detect distinct fraud archetypes. The rule-based pipeline preferentially surfaces sustained 
multi-dimensional outliers in pathology and high-volume primary care, while the autoencoder 
uniquely identifies beneficiary-churn patterns in pediatrics and pediatric dentistry—fraud types 
historically underserved by volume-and-price detection logic. The paper reports $493M in 
peer-anomalous billing across the top 100 high-confidence candidates and discusses 
methodological choices including the separation of price-per-claim from aggregate paid amount, 
the treatment of T-MSIS reporting lag, and the handling of structurally sparse peer groups that 
materially affect fraud detection output. Investigation into these individual providers is necessary 
for validation of concerns. 
Keywords: Medicaid fraud, T-MSIS, peer group analysis, autoencoder, anomaly detection, 
claims analytics, program integrity 
