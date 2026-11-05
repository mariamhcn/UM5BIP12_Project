# Raw Data — TCGA-OV Project

This folder contains the raw datasets used to investigate whether RNA-seq gene expression profiles can predict homologous recombination deficiency (HRD) in ovarian cancer.

## Data sources

| File | Description | Source |
|---|---|---|
| `TCGA-OV.star_counts.tsv` | RNA-seq gene expression matrix (STAR-Counts). Contains gene expression measurements for TCGA-OV tumor samples. Used as input features (**X**) for the prediction models. | [UCSC Xena — TCGA-OV](https://xenabrowser.net/datapages/?cohort=GDC%20TCGA%20Ovarian%20Cancer%20(OV)) |
| `TCGA_DDR_Data_Resources.zip` | Genomic DNA damage repair dataset from Knijnenburg et al. (2018). Contains HRD-related scores used to define the prediction target (**y**). The HRD score definition and classification threshold must be verified before analysis. | [GDC — PanCan-DDR-2018](https://gdc.cancer.gov/about-data/publications/PanCan-DDR-2018) |
| `clinical.tsv` | Clinical annotations for TCGA-OV patients, including demographic and disease-related information. Used to characterize the cohort and explore potential clinical associations. | [GDC Data Portal — TCGA-OV](https://portal.gdc.cancer.gov/projects/TCGA-OV) |

## Data integration

The three datasets will be matched using TCGA patient identifiers.

- **Input (X):** RNA-seq gene expression.
- **Target (y):** Genomic HRD status derived from published HRD scores.
- **Metadata:** Clinical annotations for cohort description and secondary analyses.

Only patients with matching expression data and valid HRD labels will be included in the supervised analysis.

## Reproducibility

Original files should remain unchanged in this folder. All filtering, preprocessing, normalization and patient matching will be performed in separate scripts.

Record the download date, source version and exact filenames when retrieving the datasets.

## References

[1] The Cancer Genome Atlas Research Network. (2011). Integrated genomic analyses of ovarian carcinoma. Nature, 474(7353), 609‑615. https://doi.org/10.1038/nature10166

[2] Knijnenburg, T. A. et al. (2018). Genomic and molecular landscape of dna damage repair deficiency across the cancer genome atlas. Cell Reports, 23(1), 239-254.e6. https://doi.org/10.1016/j.celrep.2018.03.076
