single_cell_visualizer.ipynd

Notebook Structure

The notebook is organized into 12 sections:

1. Setup and Imports - Load all required libraries
2. Configuration - User-editable parameters (input file, output dir, column names)
3. Load Data - Read CSV and preview the dataset
4. Auto-detect Feature Columns - Automatically identify numeric features vs metadata
5. Feature Distributions - Histograms/violin/box plots
6. Correlation Heatmap - Feature correlations
7. Clustered Heatmap - Hierarchical clustering of cells × features
8. Dimensionality Reduction - PCA, UMAP, t-SNE
9. Spatial Scatter Plot - Cells in spatial coordinates
10. Feature Comparison - Scatter plot of two features
11.Cluster Summary - Bar charts, pie charts, heatmaps by cluster
12. Summary - List of all generated outputs

Key Features
- Interactive configuration at the top of the notebook
- Auto-detection of feature columns and spatial coordinates
- Optional saving - set OUTPUT_DIR = None to just display plots
- Modular functions - each visualization is a standalone function you can customize
- Progress bars with tqdm for longer operations
- Graceful handling of optional dependencies (UMAP)

CPM_montage_creator.ipynd

Notebook Structure
The notebook is organized into 11 sections:

1. Setup and Imports - Load required libraries
2. Configuration - User-editable parameters (input dir, output path, layout options)
3. Helper Functions - Color generation, file discovery, legend building
4. Locate and Load Data - Find mask directory and cluster mapping file
5. Load Images - Load all TIFF files with progress bar
6. Build Color Legend - Auto-generate legend from mapping or image colors
7. Create Montage - Main montage generation function
8. Save Montage - Export to PNG
9. Custom Legend (Optional) - Define your own color-to-label mapping
10. Create Subset Montages (Optional) - Make montages from specific FOVs
11. Summary - Display final statistics

Key Features
- Interactive configuration at the top
- Preview cells for individual images and legend before creating montage
- Auto-detection of cluster mapping file and cell type names
- Custom legend support - define your own color-to-cell-type mapping
- Subset montages - easily create montages from specific FOVs
- Progress bars for loading images

differential_analysis.Rmd

Analysis Methods

diffcyt Package
1. Differential Abundance (DA) - Tests if cell type proportions differ between conditions using edgeR
2. Differential State (DS) - Tests if marker expression differs within cell types using limma

cytoGLMM Package
1. cytoglm - Generalized linear models with bootstrap inference
2. Per-cell-type analysis - Runs GLMM separately for each cell type

Key Features
- Auto-detects marker columns from ark-analysis cell table structure
- Creates sample metadata automatically if not provided
- Handles experimental design with patient/donor as random effects
- Multiple testing correction with adjustable FDR threshold
- Visualizations: Volcano plots, heatmaps, forest plots
- Exports results as CSV files

Required Sample Metadata Format
If providing a metadata file, it should have these columns:

sample_id	  condition	  patient_id
fov0		    Control	    Patient1
fov1		    Treatment	  Patient1
fov2		    Control	    Patient2

