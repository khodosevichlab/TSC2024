# TSC2024
Code and data accessibility for the manuscript "Single-nucleus profiling of cortical tubers in tuberous sclerosis complex shows molecular structure preservation and massive reorganization of metabolism." authored by Sørensen, FNF. et al.

## Compiled notebooks and analysis from the paper
HTML and markdown files with complete vignettes will be available upon publication.

The analysis flow is organized sequentially from 1 through 6.
If you want to skip preprocessing, you can start at `3.all_cells` and follow the scripts from there.

- `1.preprocessing`
- `2.preprocessing_cb`
- `3.all_cells`
- `4.glia`
- `5.neurons`
- `6.smFISH`

The neuron analysis workflow includes several sub-workflows:
- GWAS integration with the CELLEX/CELLECT pipeline (GWAS_CELLEX_CELLECT)
- Transcription factor inference with decoupleR/collecTRI (TF_inference)
- CellChat ligand-receptor interactions (Cellchat)
- Single-cell genotyping of probe based hybridization capture of TSC2 cDNA transcripts from same cells as used in 10x snRNA-seq (scgenotype)
- Candidate Caudal Late Inhibioty Progenitor (CLIP) cell identification (CLIP_cell_identification)
- Assesment of tissue origin signatures on expression (postmortem and surgery signatures from control and TSC patients respectively) (Tissue_origin_signatures)

Before starting these make sure to complete the previous workflows 3.all_cells, 4.glia and 5. neurons (TSC2_Neurons.rmd notebook)-

## Count matrices and other data files
Data files have been encrypted in one file `TSC2024_data.tgz` and can be downloaded here or with wget in terminal:

"https://kkh.bric.ku.dk/Frederik/TSC2/TSC2024_data_files.tgz" 

The data file folder contains folders analogous to the format as above. Each folder contains the necessary data files for the corresponding folder in the github repository.

- `0.10x_count_matrices`
- `0.cellbender_counts`
- `1.preprocessing`
- `2.preprocessing_cb`
- `3.all_cells`
- `4.glia`
- `5.neurons`
- `6.smFISH`

`10x_count_matrices` contains 10x Genomics filtered count matrices after cell calling.

`cellbender_counts` holds CellBender matrices and additional sample information from the pipeline.

Post-preprocessing and QC-filtered count matrices (`cms_final_filter.rds`) will serve as the starting object for `3.all_cells`, `4.glia`, and `5.neurons`.

## Annotations are supplied at four resolutions

- `l1` = low resolution
- `l2` = mid/low resolution 
- `l3` = mid/high resolution
- `l4` = high resolution

Annotations are stored as factors in a list (e.g., `annotation$l2`).

## All sample names are already pseudo-anonymized from the primary HPC/research institutions.


Please see the file `identifier_list.csv`.

---

--- April 2026 ---
