# DS4002 Data Science Project 3

## Overview 
This project analyzes the relationship between qualitative movie poster aesthetics (e.g., dominant color palettes, brightness, saturation, face density) and global box office performance. The analysis aims to identify whether visual design choices can reliably predict unexpected financial success, and evaluates how these visual metrics interact with critical seasonal release windows.

All analyses are conducted in a Jupyter Notebook environment, utilizing K-Means clustering for color extraction, RetinaFace neural networks for facial detection, and advanced statistical modeling (Interaction OLS Regression and Random Forest Regressor). The project is fully reproducible using the provided notebook and dataset.

## Repository Contents
The repository includes the main analysis notebook, the comprehensive movie poster datasets, extracted feature metadata, and all generated model evaluations. The structure is organized to clearly separate raw data, processing code, and presentation-ready results.

## 1. Software and Platform 
- GitHub Codespaces
- Jupyter Notebook

**Required Packages** 
- pandas
- numpy
- matplotlib
- opencv-python (cv2)
- scikit-learn
- retinaface
- statsmodels
- requests

**Platforms** 
- macOS 


## 2. Repository Structure
```text
project-root/
├── data/
│   ├── MASTER_RELEASE_SCHEDULE_UPDATE4.csv
│   ├── ALL_POSTER_METADATA.csv
│   └── FEATURE_ENGINEERED_DATA_ALL.csv
├── scripts/
│   └── imageProject.ipynb
├── README.md
└── outputs/
    └── (generated tables, OLS summaries, and figures)
```

**File Descriptions**
*   **`data/MASTER_RELEASE_SCHEDULE_UPDATE4.csv`**: This dataset is the basis for the entire project, which contains the unique film IMDb id's required to scrape the poster metadata for each film. It includes lots of information for each film, most of which is not necessary and/or relevant for this project.
*   **`data/ALL_POSTER_METADATA.csv`**: The primary dataset featuring all compiled baseline film metadata (like TMDb paths and financials) for the ~21,800 posters. NOTE: in the juptyer notebook file, this data is an overwritten version of a previous SAMPLED_POSTER_METADATA file, but the name has been changed on GitHub to avoid confusion and clarify that this file contains the metadata for ALL posters, and not a sample of them.
*   **`data/FEATURE_ENGINEERED_DATA_ALL.csv`**: The finalized dataset containing all extracted visual features (color palettes, face density, brightness, etc.) used directly in the statistical modeling.
*   **`scripts/imageProject.ipynb`**: Main Jupyter Notebook containing the data pipeline, API scraping, image analysis, and statistical modeling. NOTE: This file is split into three distinct sections: the first being the data collection/scraping, the second being the statistical analysis applied to a 1000 film sample, and the third being the statistical analysis applied to the entire poster set.
*   **`README.md`**: Project documentation and reproduction instructions.
*   **`outputs/`**: Folder containing exported high-resolution figures, regression summaries, and predictive modeling evaluation tables.

## 3. Instructions for Reproducing Results
1. Open the repository in GitHub and launch Codespaces (or clone locally).
2. Set your Python working directory to the project root folder.
3. Ensure the baseline dataset `MASTER_RELEASE_SCHEDULE_UPDATE4.csv` is located in the root or `/data` directory. Note: You must provide your own TMDb API key in the configuration block to run the web scraper.
4. Open `imageProject.ipynb`.
5. Run all cells in order.

**The notebook will:**
- Filter the baseline dataset for reliable global box office data
- Connect to the TMDb API to download thousands of movie poster images
- Filter images through an OpenCV pipeline to extract brightness, saturation, and custom "Orange/Teal" color scoring
- Utilize a RetinaFace neural network to detect and quantify "face density" per poster
- Train linear interaction models (OLS) and a Random Forest Regressor to predict log-transformed global revenue
- Export final correlation statistics, model validations, and visualizations to the outputs folder
