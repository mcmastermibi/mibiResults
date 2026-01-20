ReadMe_CPM_montage_creator

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
