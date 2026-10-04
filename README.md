# Hospital wastewater metagenomics — processed tables
 
Processed data from a cross-sectional metagenomic study of wastewater collected from
eight collection points within a tertiary hospital (Western General Hospital, Edinburgh)
and a community sewage works, sampled over 24 h with composite samplers in June 2017.
 
**Source paper:** Fisher et al. (2021), *Frontiers in Microbiology* 12:703560.
DOI: [10.3389/fmicb.2021.703560](https://doi.org/10.3389/fmicb.2021.703560)
Tables below are transcribed from the article's Supplementary Material (Data Sheet 1),
published open access under CC BY 4.0.
 
**Raw reads:** European Nucleotide Archive, see the paper's data availability statement.
 
## Files
 
| File | Contents |
|---|---|
| `TableS1_read_counts.csv` | Total, non-human, bacterial, viral, unclassified and AMR-gene read pairs per sample (8 samples) |
| `TableS2_gdna_concentration.csv` | Genomic DNA extraction concentration, ng/µl (10 samples) |
| `TableS3_taxon_counts.csv` | Taxon read counts, 1,774 taxa × 8 samples |
| `TableS4_arg_fpkm.csv` | ARG abundance in FPKM, 236 ResFinder gene groups × 8 samples |
| `sample_metadata.csv` | Collection point → site type, clinical specialties served, sampling point description |
| `Fisher2021_hospital_wastewater_tables.xlsx` | All five tables as sheets in one workbook |
 
Each table is also provided as a standalone `.xlsx`.
 
## Notes on the data
 
- ARG abundance was quantified with KMA against the ResFinder database and expressed as
  FPKM (fragments per kilobase of reference per million reads).
- Taxonomic assignment in `TableS3` is at genus level where resolvable. The table is
  reproduced exactly as published, including every row the authors reported.
- `TableS1` percentage columns from the original PDF have been dropped; compute them from
  the raw counts.
- Sample identifiers are not identical across tables. Join on `sample` and check the result.
- `sample_metadata.csv` records the sampling point for each collection point, including
  where it differs from the others.
## Provenance
 
Tables S1 and S2 were transcribed from the supplementary PDF. Tables S3 and S4 were parsed
programmatically from the same PDF (pages 13–57 and 58–62). All rows were recovered:
1,774 taxa and 236 ARG gene groups, with no duplicates. Four taxon rows whose names
collided with the first numeric column during PDF text extraction were repaired against
the source. Per-sample column sums of `TableS4` reproduce the ranking shown in the paper's
Supplementary Figure 4, and the `Homo` row of `TableS3` equals
(`all_read_pairs` − `non_human_read_pairs`) from `TableS1` for all eight samples.
 
