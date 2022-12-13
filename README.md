# DATA 512: Project
## COVID-19 Population Dynamics in King County, WA

Regina-Mae Dominguez  
UW MSDS - Autumn 2022 - DATA 512 Human Centered Data Science 

This first iteration of the final project will consist of a common analysis: "How did masking policies change the progression of confirmed COVID-19 cases from February 1, 2020 through October 1,2021?" This project will analyze this question using data for King County, WA. The data extraction, cleaning, and analysis is conducted in the Jupyter Notebook `Project.ipynb` found in the folder [Part 1](https://github.com/reginamaee/data-512-project/tree/main/Part%201). The second analysis of the project extends this further and analyzes the behaviors of different compartments with vaccination and mask usage. The data cleaning and analysis is found in the Jupyter Notebook `part2_extension_plan.ipynb` found in the folder [Extension Plan](https://github.com/reginamaee/data-512-project/tree/main/Extension%20Plan).

## Project Goals
The COVID-19 pandemic has made an impact across the world. This project
investigates the dynamics of COVID-19 in King County, WA with an initial focus on
mask usage and an extension to vaccination efforts. By using a combination of
epidemiological modeling and data science, we look at how different intervention
strategies can help control the spread of COVID-19. This analysis can provide
implications in policy prevention strategies for the community and insight for public
health officials to make informed decisions in their response to COVID as well as
influence the behaviors or decisions individuals make for the benefit of their health.

With this model, we hope to answer the following questions:
How does the introduction of vaccines affect behaviors of COVID-19 disease dynamics in King County, WA during the COVID-19 epidemic from February 2020 to October 2021? 
Does adding a masking proportion rate lower the rate at which individuals become infected?

We hypothesize that: 
The introduction of a vaccine with vaccination of at least 30% of the population, initially, will decrease the disease death rate by at least 2%.
Adding a masking proportion of at least 40% of the population will slow the spread of the disease by about 10 days. 



## Datasets
### Input Files
All data files are saved in the folder [Raw files](https://github.com/reginamaee/data-512-project/tree/main/Raw%20data)
* `RAW_us_confirmed_cases.csv`: This dataset is provided from the Kaggle repository of the [John Hopkins University COVID-19 Data](https://www.kaggle.com/datasets/antgoldbloom/covid19-data-from-john-hopkins-university).
* `U.S._State_and_Territorial_Public_Mask_Mandates_From_April_10_2020_through_August_15_2021_by_Country_by_Day.csv`: This dataset is obtained from the [Center of Disease Control](https://data.cdc.gov/Policy-Surveillance/U-S-State-and-Territorial-Public-Mask-Mandates-Fro/62d6-pm5i) and contains policy information of mask mandates for several locations. (Note: this`csv` is relatively big to upload onto Github, should download directly from link)
* `mask-use-by-country.csv`: This dataset is from the New York Times and describes the results of their [mask compliance survey](https://github.com/nytimes/covid-19-data/tree/master/mask-use) data.
* `vax_public.csv`: This dataset is derived from the [King County, WA government website](https://kingcounty.gov/depts/health/covid-19/data.aspx) and contains information about daily vaccination dosages. 
* `COVID19_King-County.csv`: This dataset is derived from the [King County, WA government website](https://kingcounty.gov/depts/health/covid-19/data.aspx) and obtains all information about COVID-19, with daily case values and deaths.

Other data sources used in this study come from the [Washington Department of Health](https://doh.wa.gov/data-and-statistical-reports/washington-tracking-network-wtn) and the [Center for Disease Control and Prevention](https://www.cdc.gov/coronavirus/2019-ncov/index.html)
These datasets are free for download and use.

### Licenses and Terms of Use
* [John Hopkins University COVID-19 Data](https://www.kaggle.com/datasets/antgoldbloom/covid19-data-from-john-hopkins-university) is licensed with Attribution 4.0 International (CC BY 4.0), the Creative Commons License.
* [The NY Times](https://github.com/nytimes/covid-19-data/tree/master/mask-use) provides the mask usage dataset under the terms of non-commerical purposes and credit to be given to the New York Times. More information can be provided [here](https://github.com/nytimes/covid-19-data/blob/master/LICENSE).


The King County, WA COVID-19 data i s a compilation of data from the Washington Department of Health.
* [Washington Department of Health](https://doh.wa.gov/node/8511) states that data is accessible to the public. (In the State of Washington, laws exist to ensure that government is open and that the public has a right to access appropriate records and information possessed by state government.)

## Data & Project Considerations 
* This project is conducted only for King County, WA. Data should be subsetted accordingly.
* When getting case values from the John Hopkins University data, the case value should be by each day and represent the cumulative number of cases. In some instances, a more recent date will have a lower number of cases from a previous date, these dates were corrected using linear interpolation (as shown in the notebook).
* The mask mandate policy stopped tracking on 08/15/2021. This may not reflect the true instance when the mask mandate ended in a specific county.
* The King County WA data may have underreporting as Seattle and King County data have encountered a security breach from one of Washington's hospital organizations.


### Python Packages
Please install the following Python packages through `pip install` or `conda install`
* `pandas`
* `numpy`
* `matplotlib`
* `seaborn`
* `ruptures` (needed only in `Project.ipynb`)
* `scipy.integrate` (needed only in `part2_extenstion_plan.ipynb`)


