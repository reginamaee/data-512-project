# DATA 512: Project
## Project Part 1: Common Analysis

Regina-Mae Dominguez  
UW MSDS - Autumn 2022 - DATA 512 Human Centered Data Science 

This first iteration of the final project will consist of a common analysis: "How did masking policies change the progression of confirmed COVID-19 cases from February 1, 2020 through October 1,2021?" This project will analyze this question using data for King County, WA. The data extraction, cleaning, and analysis is conducted in the Jupyter Notebook `Project.ipynb`.

## Datasets
### Input Files
* `RAW_us_confirmed_cases.csv`: This dataset is provided from the Kaggle repository of the [John Hopkins University COVID-19 Data](https://www.kaggle.com/datasets/antgoldbloom/covid19-data-from-john-hopkins-university).
* `U.S._State_and_Territorial_Public_Mask_Mandates_From_April_10_2020_through_August_15_2021_by_Country_by_Day.csv`: This dataset is obtained from the [Center of Disease Control](https://data.cdc.gov/Policy-Surveillance/U-S-State-and-Territorial-Public-Mask-Mandates-Fro/62d6-pm5i) and contains policy information of mask mandates for several locations. (Note: this`csv` is relatively big to upload onto Github, should download directly from link)
* `mask-use-by-country.csv`: This dataset is from the New York Times and describes the results of their [mask compliance survey](https://github.com/nytimes/covid-19-data/tree/master/mask-use) data.

## Data & Project Considerations 
* This project is conducted only for King County, WA. Data should be subsetted accordingly.
* When getting case values from the John Hopkins University data, the case value should be by each day and represent the cumulative number of cases. In some instances, a more recent date will have a lower number of cases from a previous date, these dates were corrected using linear interpolation (as shown in the notebook).

### Python Packages
Please install the following Python packages through `pip install` or `conda install`
* `pandas`
* `numpy`
* `matplotlib`
* `seaborn`
* `ruptures`
