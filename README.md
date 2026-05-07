# PepSurf_G ∪ EpiSearch Colab - Analysis Workflow
This folder contains a ready-to-run Google Colab notebook that guides users through a full PepSurf_G + EpiSearch epitope analysis workflow, from PepSurf and EpiSearch outputs to union epitope prediction and optional 3D visualization.

## Main notebook
- PepSurf_G_U_EpiSearch_Colab.ipynb

## What this notebook does
- Loads PepSurf outputs and builds a minimal peptide set using a Greedy Algorithm (PepSurf_G).
- Processes EpiSearch results and merges them with PepSurf_G.
- Generates the union epitope table and exports CSV + Excel.
- Optionally visualizes epitope residues on a 3D structure (PDB).

## Inputs required
From PepSurf analysis:
- pepSurfServer.res
- *_significantPaths.txt

From EpiSearch analysis (best solution copied to a text file):
- <antigen_name>_episearch.txt

Optional:
- A .pdb file for 3D visualization.

## Software to generate PepSurf inputs
You have to run PepSurf locally before using the notebook.
Downloads (Windows): https://github.com/aldemobr/PepSurf_G-EpiSearch---Analysis-Workflow/blob/cb5f4f431c4d557158e5dc38138ef1783382fb4d/PepSurf_softwares_download.zip

## How to run (Colab)
1. Open the notebook in Google Colab.
2. Run cells from top to bottom.
3. Upload pepSurfServer.res and *_significantPaths.txt.
4. Enter the antigen name.
5. Run the PepSurf_G step and download the results.
6. Run EpiSearch externally (webserver) using the peptides classified as Required (minimal set) and save:
   <antigen_name>_episearch.txt
7. Upload the EpiSearch file and run the union steps.
8. Download the final union CSV and Excel files.
9. (Optional) Upload a PDB file to visualize the epitope residues.

## Outputs
- <antigen_name>_minimal_peptides.csv
- <antigen_name>_minimal_peptides_details.txt
- <antigen_name>_episearch_processed.txt
- <antigen_name>_combined_pepsurf_episearch_union.csv
- <antigen_name>_combined_pepsurf_episearch_union.xlsx

## Notes
- The notebook uses Colab form-style cells so large script blocks are collapsible.
- Filenames must match exactly as listed above.
