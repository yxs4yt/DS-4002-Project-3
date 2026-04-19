# DS4002 Data Science Project 3

## Overview 
This project analyzes crime data to examine how crime patterns vary by season and time of day. The analysis focuses on identifying when crime is most prevalent, the most common types of crimes, and how timing and seasonality interact with crime categories.

All analyses are conducted in a Jupyter Notebook environment, where the data is cleaned, timestamps are processed, and visualizations are generated. The project is fully reproducible using the provided notebook and dataset.

## Repository Contents
The repository includes the main analysis notebook, the dataset used for the project, and any generated outputs. The structure is organized to clearly separate raw data, code, and results.

## 1. Software and Platform 
- GitHub Codespaces
- Jupyter Notebook

# Required Packages 
- pandas
- matplotlib
- seaborn
- scipy

# Platforms 
- MacoS

## 2. Repository Structure
project-root/
├── data/
│   └── Master_Release.csv
├── analysisplan.ipynb
├── README.md
└── output/
    └── (generated tables or figures)

**File Descriptions**
data/Master_Release.csv: Primary dataset used for all analyses (only relevant dataset).
analysisplan.ipynb: Main Jupyter Notebook containing all data cleaning, analysis, and visualizations.
README.md: Project documentation and reproduction instructions.
output/: Folder for any generated figures or exported results.

**3. Instructions for Reproducing Results**
1. Open the repository in GitHub and launch Codespaces.
2. Set the working directory to the project root folder.
3. Ensure the dataset Master_Release.csv is located in the data/ folder.
4. Open analysisplan.ipynb.
5. Run all cells in order.

The notebook will:
- Load and clean the crime dataset
- Extract and structure timestamp information
- Analyze crime trends by season and time of day
- Identify the top 5 most common crimes
- Visualize relationships between crime type, timing, and season
- Perform statistical analysis (including t-tests) to evaluate differences in crime patterns
