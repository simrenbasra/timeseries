# Data Processing Overview

This folder contains a series of notebooks designed to process and prepare Microsoft stock data for analysis and forecasting.
Below is a detailed description of each notebook within this folder:

## Notebooks Overview

### 01-data-loading

**Purpose:**  
Loads the Microsoft stock data from the yFinance library in Python. This notebook ensures that the original data is imported correctly, with the date set as the index. It also provides preliminary insights into the stock data to help gain an understanding of the data.

**Output:**  
- The original dataset with a datetime index, saved for further processing and analysis.

---

### 02-data-cleaning

**Purpose:**  
Handle necessary data cleaning tasks. This includes addressing missing dates and values to ensure the data is continous across all dates.

**Output:**  
- A cleaned version of the original data. Note that the data remains non-stationary at this stage.

---

### 03-data-eda

1. Exploratory Data Analysis (EDA): Conduct initial visualisations and statistical analyses on the cleaned, non-stationary data. This includes plotting timeseries data to identify trends, seasonality and patterns to gain insights into the data.

2. Seasonal Trend Decomposition: Decompose the timeseries data into its trend, seasonality and residual components to better understand the trend and patterns in the data.

3. Stationarisation and Differencing: Apply transformations such as differencing and boxcox to make the data stationary, which is required for forecasting models like ARIMA. 

**Output:**  
- Stationary version of the dataset, ready for forecasting 

## Usage

**Run Notebooks Sequentially:** Follow the order of notebooks to process the data from loading through cleaning and EDA to final preparation for forecasting.

For further details on each notebook's content and execution, refer to the respective notebook files in this folder.
