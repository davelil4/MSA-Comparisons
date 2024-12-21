---

# Project: Comparative Analysis of Sequence Alignment Tools Using Profile HMM and MSA Techniques

This project implements and evaluates sequence alignment methods using the BaliBase dataset (RV11 and RV12 subsets). The notebook compares the performance of multiple sequence alignment (MSA) tools (MAFFT, Muscle, ClustalW) with probabilistic alignment methods, including a custom Profile Hidden Markov Model (ProfileHMM) implementation and HMMER. Key metrics such as sum-of-pairs (SP) and column scores (TC), runtime, and Leave-One-Out Cross Validation (LOOCV) are used to assess performance.

## Requirements

### Conda Environment

The project includes an `environment.yml` file to set up the required dependencies. The environment installs tools like `mafft`, `clustalw`, and `muscle` via conda, while Python libraries (e.g., `Biopython`, `pyHMMER`) are installed using pip inside the conda environment.

1. **Create the Environment**:
   Run the following commands to create and activate the environment:
   ```bash
   conda env create -f environment.yml
   conda activate biovenv
   ```

2. **Verify Installation**:
   Ensure all tools and libraries are installed by checking the environment:
   ```bash
   conda list
   ```

### Dataset

Ensure the BaliBase RV11 and RV12 datasets are downloaded and placed in the appropriate directory structure:
```
bb3_release/
├── RV11/
│   ├── test_case_1.tfa
│   ├── test_case_1.msf
│   ├── ...
├── RV12/
│   ├── test_case_1.tfa
│   ├── test_case_1.msf
│   ├── ...
```

## How to Run

1. **Open the Notebook**:
   Launch Jupyter Notebook using the conda environment:
   ```bash
   conda activate final_proj_env
   jupyter notebook
   ```
   Open `Final_Proj_Clean.ipynb` in the Jupyter interface.

2. **Run the Notebook**:
   Execute all cells in the notebook sequentially. The notebook is designed to:
   - Train and test alignments using the custom ProfileHMM.
   - Generate alignments with HMMER, MAFFT, Muscle, and ClustalW.
   - Calculate LOOCV SP and TC scores.
   - Compare results across RV11 and RV12 datasets.
   - Generate and save graphical visualizations of performance metrics.

3. **Outputs**:
   - **Graphs**: SP and TC scores, runtime comparisons, and LOOCV results are saved as `.png` files in the working directory.
   - **Data**: Tabulated results for SP, TC, and runtime metrics are displayed in the notebook.

## Expected Results

Running the notebook reproduces the following:
- Comprehensive SP and TC score comparisons for all tools.
- Runtime analysis for training and testing phases.
- Visualizations of performance metrics for RV11 and RV12 datasets.

This setup ensures reproducibility and ease of use, allowing you to rerun the analysis by following the steps above.

---