# BEE2041 Empirical Project
## Has the Rate of Improvement in Sprint Events Slowed Compared To Endurance Events?
A data-driven investigation into performance trends in athletics. Aiming to compare improvement rates in sprint and endurance events from 1978 to 2025. 

### Blog Post
The blog post for this project can be found [here](https://hackmd.io/@crEMM-S2Sk6xpNcDdfPDrw/r1KpJ2hpWg)

### Data Source
My data was scraped from [Alltime Athletics](https://www.alltime-athletics.com/) (Peter Larsson, 1997-2026) for academic research purposes only as part of this BEE2041 Empirical Project

### Project Structure
```
.
├── README.md
├── analysis.ipynb
├── data
│   ├── processed
│   │   ├── athletics_clean.csv
│   │   └── regression_results.csv
│   └── raw
│       └── athletics_raw_complete.csv
└── figures
    ├── boxplot_times.png
    ├── combined_improvement.png
    ├── event_counts.png
    ├── event_counts_by_gender.png
    ├── female_events_pct_improvement.png
    ├── male_events_pct_improvement.png
    ├── performances_per_year.png
    ├── rate_of_improvement.png
    └── split_regression.png
```

### How to Replicate
1. Clone the repository:  
   git clone https://github.com/elliebeynonn/2041_data_project

2. Navigate to the project folder:  
   cd 2041_data_project

3. Launch Jupyter:  
   jupyter notebook

4. Open analysis.ipynb and run all cells from top to bottom using Kernel -> Restart & Run All  
This will scrape the data, clean it, produce all the figures and run the regression analysis.  
Note: The scraping section takes approximately 2-3 minutes to run because of a two second pause between requests.

#### To skip re-scraping
The raw data is already included in data/raw/athletics_raw_complete.csv. To use it instead of re-scraping, find this line in analysis.ipynb:  
df_raw = pd.read_csv("data/raw/athletics_raw_complete.csv")  
Skip the scraping cells and run everything else from top to bottom.

### Requirements
Install the required packages by running the first cell in analysis.ipynb or running this command in your terminal:  
pip install requests beautifulsoup4 pandas matplotlib seaborn scipy tabulate --break-system-packages
