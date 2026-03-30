code -> RDC.ipynb contains Python code within a notebook format to:
- Download the Appropriate Python Packages
- Transform Raw Data to Clean Data
- Export cleaned tables into cleaned csv. files: format: variable_type/variable_name
- Run all cells sequentially for results

data/raw -> contains raw excel files split into 3 categories: Dependent, Independent and Control. Datasets should not be modified and contains all original data from the Organisation for Economic Co-operation and Development (OECD) and World Bank (WB)

### Dependent Variables (2019–2024)
- % Change in Manufacturing Employment  
- % Change in Manufacturing Output  

### Independent Variables
- Labour Market Coordination (COORD)  
- Union Density  
- Collective Bargaining Coverage  

### Control Variables
- Export Dependence  
- GDP Growth (%) 


data/clean -> contains the newly cleaned .csv files after running the code:RDC.ipynb

Important notes: Missing data in COORD from 2020 - 2024 is resolved by using 2019 data as a proxy. COORD is a time in-variant variable, and therefore it is appropriate for this case.

Environment uses Python 3.10+