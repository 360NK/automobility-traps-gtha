# GGR376 Final Project: Automobility Traps in the GTHA

GGR376H5 Spatial Data Science II, University of Toronto Mississauga, Winter 2026

Janiri Nunal, Gurman Sanga, Tissan Kugathas, Kashy Namboothiri

---

## What this project is about

Low-income households are supposed to rely less on cars. In the GTHA, that does not always hold. A lot of the region's affordable housing sits far from the Metrolinx rapid transit network, which means driving is less of a choice and more of a necessity. We call this an automobility trap.

We looked at 1,512 Census Tracts across the Toronto, Hamilton, and Oshawa CMAs to test how much of that pattern is explained by household income and distance to the nearest transit station. The analysis runs through spatial clustering, a baseline OLS model, spatially-aware XGBoost, and GeoShapley to break down what is actually driving the predictions at the tract level.

## Repo structure

```
GGR376_Final_Project.ipynb   main analysis notebook
data/
  chass/           2021 Census commuting and income data (CHASS export)
  census_tracts/   StatsCan 2021 Census Tract boundaries
  frtn/            Metrolinx FRTN station points and line features
outputs/           GeoPackage and CSV outputs from each section
```

## Data sources

- Statistics Canada 2021 Census via CHASS, commuting mode and median household income
- Statistics Canada 2021 Census Tract boundaries, catalogue no. 92-168-X
- Metrolinx Frequent Rapid Transit Network 2022, station points and line features

## Running the notebook

The notebook was developed and run in Google Colab with Google Drive. All the outputs from that run are already embedded in the notebook, so you can open it and read through the results without running anything.

If you want to re-run it in Colab, Cell 2 uses the Drive mount as written. To run it locally instead, Cell 2 has the local paths as a commented-out block you can swap in.

Dependencies:
```
pip install geopandas libpysal esda mapclassify statsmodels xgboost scikit-learn shap geoshapley joblib splot
```
