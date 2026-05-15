This is a unit project for ECC3146

## Research Design

Research Question: Does higher labour market coordination improve labour market resilience in advanced economies?
Countries Data Used: Germany, Netherlands, Belgium, Austria, Denmark, Sweden, Norway, Finland, Japan, South Korea, Switzerland, USA, UK, Canada, Australia, New Zealand
Years: 2000 - 2023

Comparability: The sample consists of advanced economies with differing labour market coordination structures, allowing comparison across liberal, coordinated, and corporatist institutional systems while maintaining comparable levels of economic development. The sample covers 2000–2023, to analyse and compare labour market resilience across countries before, during, and after major economic shocks, including the Global Financial Crisis and COVID-19.

The sample was selected to maximize variation in labour market coordination while maintaining comparable levels of economic development. Country fixed effects are included to control for time-invariant country characteristics, while year fixed effects control for global shocks affecting all countries simultaneously.


## Variables

Dependent Variable
- Change in unemployment rate
    - World Bank indicator: SL.UEM.TOTL.ZS

Main Independent Variable
- Labour market coordination (COORD)
    - Source: ICTWSS Database

Control Variables
- GDP growth
- Inflation
- Export dependence
- Government spending

All macroeconomic variables are sourced from the World Bank World Development Indicators database.

## Replication Instructions
1. All Datasets are pre-downloaded into data/raw, unmodified

2. Required Packages

- pandas
- numpy
- statsmodels
- matplotlib
- seaborn
- pathlib

Install with:

```bash
pip install pandas numpy statsmodels matplotlib seaborn

3. Run all code in RDC.ipynb --> outputs clean files into data/clean

4. Run `Primary Econometric Analysis.ipynb` to reproduce the regression results and regression table.

##Primary Economic Analysis

This notebook:
- Loads `data/clean/final_panel.csv`
- Declares the analysis as descriptive
- Estimates the baseline fixed-effects regression
- Reports the regression table
- Interprets the main coefficients
- Discusses threats and limitations

5. Run `Robustness Analysis.ipynb` for robustness checks
This notebook:
- loads `data/clean/final_panel.csv`
- Runs a set of Robustness Checks
- Produces a Robustness Tables, a summary of the results for the Robustness Checks (leave_one_country_out.csv) and (robustness_table.csv)
- Inteprets the Robustness Tables Results