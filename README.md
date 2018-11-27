# Analysis of Gapminder per capita CO2 data

This project involves data wrangling several Gapminder datasets into one long-format CSV. This data is then analyzed with Pandas, Numpy, Plot.ly + Cufflinks, as well as Seaborn. 

All work is in jupyter notebooks.

While all data wrangling is painful, the initial matching of region & sub-region values (e.g. 'Europe' & 'Western Europe') to country names was so particularly painful that I've documented it iin a separate file, to not distract from the flow of the data analysis.

For the same reasons, the wrangling into long format & batch-merging of multiple Gapminder datasets is also done in a separate notebook.

## File structure

**/gapminder**:

* **analyze_CO2.ipynb**: Loads `data/final_df.csv` and analyzes first only `CO2_pc`, then `CO2_pc` by region & sub-region, then does multi-variate analyses with variables for energy, income, and standard-of-living.

* **analyze_CO2.html**: HTML export of above notebook.

* **make_df.ipynb**: batch converts csv & xls files into dataframes, cleans them and converts to long format. It then merges them, then does partial-string matching to ensure all countries have values for the region & sub-region columns. Outputs `final_df.csv`.

* **make_df.html**: HTML export of above notebook.

* **/data**:

   * **/merge_regions**: contains jupyter notebook & .csv files. The notebook documents the merging of regions data with the Gapminder CO2 dataset. Outputs `countries_with_regions.csv`, which is used by `make_df.ipynb`.
   * **/originals**: contains original .csv/.xls files downloaded from gapminder. Input for `make_df.ipynb`.
   * **final_df.csv**: output of `make_df.ipynb`



