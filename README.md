## Predicting Multiple Sclerosis from Radiologically Isolated Syndrome using Generative Manifold Learning

This repository accompanies our study investigating whether generative manifold learning applied to brain MRI can stratify individuals with Radiologically Isolated Syndrome (RIS) according to their risk of conversion to clinical multiple sclerosis (MS).

RIS is characterized by incidental MRI findings suggestive of MS in asymptomatic individuals. Although a substantial proportion of RIS subjects eventually develop clinical symptoms, predicting individual conversion risk remains challenging. In this work, we applied an unsupervised generative artificial intelligence framework (BrainGML-MS) to model individualized structural brain deviations from a normative reference population.

The method combines deep learning–based brain segmentation (AssemblyNet) with nonlinear manifold learning to construct a low-dimensional representation of whole-brain morphometry. For each subject, a personalized “digital twin” is generated using nearest neighbors from a large healthy reference dataset. This enables computation of regional z-score deviations and estimation of the Brain Age Gap (BAG), defined as the difference between predicted brain age and chronological age.

Using manifold-embedded representations of RIS subjects, we performed unsupervised clustering (k-means), identifying subgroups with distinct 5-year conversion risks. We further modeled structural progression trajectories along a pseudo-temporal axis derived from geodesic distances within manifold space. Our results demonstrate a graded continuum from healthy controls to RIS non-converters, RIS converters, and MS patients, with increasing structural abnormality burden and higher BAG values in converter-like profiles.

## Data Shared in This Repository

To support transparency and reproducibility, this repository provides:

 - The low-dimensional manifold coordinates (reduced space embeddings) for all included subjects

 - Cluster assignments derived from unsupervised k-means clustering

 - Associated clinical variables, including conversion status, demographic data, lesion characteristics, and available biomarker information

Derived structural deviation metrics (e.g., BAG and abnormal ROI counts)

Raw MRI data and proprietary BrainGML-MS software are not distributed due to regulatory and intellectual property constraints. However, the shared reduced-space coordinates and clustering outputs enable independent statistical validation, downstream modeling, and methodological benchmarking.

This repository aims to facilitate reproducible research on normative modeling, AI-driven risk stratification, and the preclinical-to-clinical continuum of multiple sclerosis.
