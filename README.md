code -> RDC.ipynb contains Python code within a notebook format to:
- Download the Appropriate Python Packages
- Transform Raw Data to Clean Data
- Export cleaned tables into cleaned csv. files: format: variable_type/variable_name
- Run all cells sequentially for results

data/raw -> contains raw excel files split into 3 categories: Dependent, Independent and Control. Datasets should not be modified and contains all original data from the Organisation for Economic Co-operation and Development (OECD) and World Bank (WB)

### Dependent Variables (2019–2024)
- % Change in Manufacturing Employment  
Due to Missingness (Germany 2020), I use an extract Impute from Trading Economics 2020 Q4. Although, the base data sets were pulled from OECD, although from different parts of the website (due to the odd missingness in the different interfaces, but it is still derived from the same dataset)

Dataset 1 (OECD):https://www.oecd.org/en/data/indicators/employment-by-activity.html
Dataset 2 (OECD): https://data-explorer.oecd.org/vis?lc=en&pg=0&tm=Employment%20by%20activity&snb=329&vw=tb&df[ds]=dsDisseminateFinalDMZ&df[id]=DSD_ALFS%40DF_ALFS_EMP_ISIC&df[ag]=OECD.SDD.TPS&df[vs]=1.1&dq=.EMP..N._T.Y_GE15._T.ATU%2BBTF%2BC.A&lom=LASTNPERIODS&lo=5&to[TIME_PERIOD]=false
Dataset 3 (Trading Economics): https://tradingeconomics.com/germany/employment-manufacturing-eurostat-data.html

Due to the lack of Download Availability, the data was extracted straight off the Trading Economics site. For future robustness checks, it will likely require surface level data checks between Employment at different times. However, it is to note that this estimate is sourced from other reputable sites such as: National Statistics, EuroStat, World Bank.


### Independent Variables
- Labour Market Coordination (COORD)  
- Union Density  
- Collective Bargaining Coverage  

Dataset 1:https://www.oecd.org/en/data/datasets/oecdaias-ictwss-database.html

### Control Variables
- Export Dependence  

Dataset 1: https://data.worldbank.org/indicator/NE.EXP.GNFS.ZS?end=2025&locations=DE.&name_desc=false&start=2025&type=shaded&view=bar&year=2025

- GDP Growth (%) 

Dataset 1:https://data.worldbank.org/indicator/NY.GDP.MKTP.KN?locations=DE-US-SE&view=map

- Change in Manufacturing Output (Value of %GDP)
Due to Missingness (US 2022 - 2023 in Value of %GDP) + Future Robustness Checks, another US dataset is tabulated and cleaned for future use. The missingness in the Value of %GDP for the OECD dataset is filled in with the FRED dataset (2022 - 2023)

Dataset 1:https://data.worldbank.org/indicator/NV.IND.MANF.ZS
Dataset 2:https://fred.stlouisfed.org/series/VAPGDPMA#

data/clean -> contains the newly cleaned .csv files after running the code:RDC.ipynb

Important notes: Missing data in COORD from 2020 - 2024 is resolved by using 2019 data as a proxy. COORD is a time in-variant variable, and therefore it is appropriate for this case.

Environment uses Python 3.10+