# DS4002 Data Science Project 2

## Overview 
This project analyzes a dataset of crime postings to examine in which season and time of day crime is the most prevelaqnt. Using Jupyter through Codespaces, the project cleans the crime data, extracts and structures the time stamps, and visualizes the results. The analysis is fully script-driven and can be reproduced from the provided dataset and code.

## Repository Contents
The repository contains the Jupyter analysis file, the input dataset, and all derived outputs generated during analysis. The structure is designed to separate raw data, processing code, and results to support clarity and reproducibility.

## 1. Software and Platform 
- Codespaces
- Jupyter Notebook

# Required Packages 
- pandas
- matplotlib
- seaborn
- os
- scipy.stats
- ttest_ind

# Platforms 
- MacoS

## 2. Repository Structure
project-root/ ├── dc_crime_cleaned.csv ├── analysisplan.ipynb ├── README.md └── output/ └── (generated tables or figures, if rendered)

- dc_crime_cleaned.csv: Cleaned dataset containing relevant crime information.
- analysisplan.ipynb : Primary analysis script written in Jupyter Notebook.
- README.md: Project documentation and reproduction instructions.
- output/: Directory for rendered outputs such as HTML reports or figures.

## 2. Instructions for Reproducing Results
1. Open GitHub and navigate to Codespaces
2. Set the working directory to the project root folder.
3. Ensure the dataset file dc_crime_cleaned.csv is located in the project root directory.
4. Open the file analysisplan.ipynb in CodeSpaces.
5. The script will:
      - Load the dataset  
      - Clean and structure crime information
      - Produce output and visuals related to which season and timing is most popular for crime
      - Produce the top 5 most common crimes
      - Visualize which combination goes with each crime
      - Produce a t statistic and p value regarding the data
