# Into Data Analysis — Workbook (Luke Barousse)

This repository contains a workbook for the "Python for Data Analytics" course by Luke Barousse. It is a collection of Jupyter notebooks that explore pandas workflows, pivot tables, merging, exploding lists, applying functions, and a small project section.

## Repository structure

- [environment.yml](environment.yml) — conda environment used by the notebooks  
- [kernel_diagnostic.txt](kernel_diagnostic.txt) — kernel diagnostics / crash logs
- [test.ipynb](test.ipynb) — quick test notebook
- 1_Basics/
  - [Getting_Started.ipynb](1_Basics/Getting_Started.ipynb)
- 2_Advanced/
  - [1_Pandas_Accessing_Data.ipynb](2_Advanced/1_Pandas_Accessing_Data.ipynb)
  - [2_Pandas_date_Cleaning.ipynb](2_Advanced/2_Pandas_date_Cleaning.ipynb)
  - [3_4_Pandas_Pivot_Table.ipynb](2_Advanced/3_4_Pandas_Pivot_Table.ipynb)
  - [5_Pandas_Index_Management.ipynb](2_Advanced/5_Pandas_Index_Management.ipynb)
  - [6_Pandas_Exercise_Job_Demand.ipynb](2_Advanced/6_Pandas_Exercise_Job_Demand.ipynb)
  - [7_Pandas_Merge_Data_Frame.ipynb](2_Advanced/7_Pandas_Merge_Data_Frame.ipynb)
  - [10_Pandas_applying_Functions.ipynb](2_Advanced/10_Pandas_applying_Functions.ipynb)
  - [11_Pandas_Explode.ipynb](2_Advanced/11_Pandas_Explode.ipynb)
  - [12_Exercise_Trending_Skills.ipynb](2_Advanced/12_Exercise_Trending_Skills.ipynb)
- 3_Project/ — project materials (notebooks / assets)

## Quick start

1. Create the conda environment:
   ```
   conda env create -f environment.yml
   conda activate <env-name>  # see environment.yml 'name' or use the created env
   ```
   (See [environment.yml](environment.yml).)

2. Open the notebooks in VS Code (Jupyter extension) or JupyterLab/Notebook:
   - Recommended kernels noted in notebook metadata (e.g. `data_py311`, `python3`).

3. The notebooks load the dataset with:
   ```
   from datasets import load_dataset
   dataset = load_dataset("lukebarousse/data_jobs")
   df = dataset["train"].to_pandas()
   ```
   (Search the notebooks for `load_dataset` to see usage.)

## Notes & troubleshooting

- If a kernel crashes, check [kernel_diagnostic.txt](kernel_diagnostic.txt) for logs.
- Small parsing steps (e.g. converting `job_skills` from strings to lists) use `ast.literal_eval` in several notebooks.
- Example test run: open [1_Basics/Getting_Started.ipynb](1_Basics/Getting_Started.ipynb) and run the first cells to load the data.

## Contact / Attribution

Workbook based on content by Luke Barousse.
