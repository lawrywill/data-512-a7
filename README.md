# README for DATA 512 A7 Project

## Introduction
The analysis documented in this repository focuses on how Cuyahoga County, Ohio has been disrupted by the pandemic. In this reposistory you'll find the results of the analysis, as well as all of the documentation and code necessary for reproducing the analysis. This analysis was produced as a series of assignments for DATA512 at the University of Washington:

* __Assignment_A4__: A collaborative analysis in which students in this class examined the impact of masking requirements on the spread of COVID-19 in a specific US county (in my case, Cuyahoga county, Ohio)
* __Assignment_A5__: An extension plan for A4. My extension plan focused on the impact of COVID-19 on unemployment in Cuyahoga.
* __Assignment_A6__: A presentation of the results of the analysis proposed in the extension plan.
* __Assignment_A7__: A final report comprehensively documenting the entire process

In order to understand the full scope and results of what was analyzed, I recommend starting with the 'Final Report' pdf.

## Source data descriptions
Explanation and links for data sources are noted below. A few data sources were used for exploration but not used for the final analysis, which is also noted below.

* The raw US confirmed COVID-19 cases comes from this file from the Kaggle repository of John Hopkins University COVID-19 data: https://www.kaggle.com/antgoldbloom/covid19-data-from-john-hopkins-university?select=RAW_us_confirmed_cases.csv
* The dataset of masking mandates by county comes from the CDC website: https://data.cdc.gov/Policy-Surveillance/U-S-State-and-Territorial-Public-Mask-Mandates-Fro/62d6-pm5i
* Mask compliance survey data comes from The New York Times (not used in final results, not required for reproducing this analysis): https://github.com/nytimes/covid-19-data/tree/master/mask-use
* Monthly unemployment rates for each of the counties in the Cleveland-Elyria metropolitan area comes from the FRED (Federal Reserve Economic Data) website maintained by the Federal Reserve Bank of St. Louis:
	* Cuyahoga county: https://fred.stlouisfed.org/series/OHCUYA5URN
	* Geauga county: https://fred.stlouisfed.org/series/OHGEAU5URN
	* Lake county: https://fred.stlouisfed.org/series/OHLAKE2URN
	* Lorain county: https://fred.stlouisfed.org/series/OHLORA3URN
	* Medina county: https://fred.stlouisfed.org/series/OHMEDI0URN
	* Cleveland-Elyria metropolitan area (not used in final results, not required for reproducing this analysis): https://fred.stlouisfed.org/series/CLEV439URN


## Description of files and folders in this repository
* __LICENSE__: MIT license for this project
* __Common_Analysis.pdf__: (Also known as Assignment A4) Analysis done in collaboration with the rest of the class that looks into whether masking requirements had an impact on the spread of COVID-19 in Cuyahoga
* __Extension_Plan.pdf__: (Also known as Assignment A5) Plan that details how the 'Common Analysis' was extended to answer questions about the COVID-19 impact on unemployment in Cuyahoga
* __Final_Presentation.pdf__: (Also known as Assignment A6) Results from the 'Final Report' summarized in a 12-slide presentation format
* __Final_Report.pdf__: (Also known as Assignment A7) Comprehensive report, based on the 'Common Analysis' and the 'Extension Plan', of the impact of mask requirements on COVID-19, and the impact of COVID-19 on unemployment, in Cuyahoga. This report contains an explanation of methodologies, results, background sources, and data used.
* __hcds-a7-covid.ipynb__: Jupyter notebook containing all of the code used for the 'Final Report' (and by extension, the 'Common Analysis').
*__US_County_Assignments.csv__: CSV file containing county assignments for this analysis. My assignment was Cuyahoga county, Ohio. This file is used by hcds-a7-covid.ipynb to determine which county to use when filtering the other data sources.
* __viz__: Folder containing the data visualizations generated for the 'Common Analysis'

## Reproducing this analysis using hcds-a7-covid.ipynb
The hcds-a7-covid.ipynb notebook contains all of the code needed to reproduce this analysis. The data used is not kept in this repository, but is publicly available at the links provided above. To reproduce this analysis, download the data files from the provided links and place those files in a subfolder named 'data' (or else alter the code in the notebook to point to wherever you have stored the files). Make sure all necessary Python packages are installed, then run this notebook.

Most of the Python packages used in this analysis are common, but the pycausalimpact package used for counterfactual analysis will not be installed on most machines by default. pycausalimpact can generally be installed with a simple 'pip install pycausalimpact' command. This goes for the rest of the packages used as well. More information on pycausal impact is available at this link: https://pypi.org/project/pycausalimpact/
