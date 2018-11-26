# Analysis of Gapminder per capita CO2 data

This project involves a lot of data wrangling to clean & merge several datasets into one long-format CSV. This data is then analyzed with Pandas, Numpy, Plot.ly + Cufflinks, as well as Seaborn. 

All work was done in ipython notebooks.

While all data wrangling is painful, the matching of region & sub-region values (e.g. 'Europe' & 'Western Europe') to country names was so particularly painful that I've documented it a separate file, so as to not distract the flow of the data analysis.

For the same reasons, the wrangling into long format & batch-merging of multiple Gapminder datasets is also done in a separate notebook.

## File structure

* **/**:

* **make_df.ipynb**: batch converts csv & xls files into dataframes, cleans them and converts to long format. It then merges them, then does partial-string matching to ensure all countries have values for the region & sub-region columns. Outputs `CO2_final_nov18.csv`.

* **investigate_CO2_2013_nov18.ipynb**: Loads `CO2_final_nov18.csv` and analyzes first only `CO2_pc`, then `CO2_pc` by region & sub-region, then does multi-variate analyses with variables for energy, income, and standard-of-living.

* **/data**:

  * **/updates_nov18**: contains original .csv/.xls files downloaded from gapminder.
  * **/final_nov18**: stores the output of `make_df.ipynb`



