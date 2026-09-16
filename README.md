# Lab 2: Analysis Notebook — Framingham Heart Study (teaching subset)

**Course:** PUBH 4201
**Dataset:** Framingham Heart Study teaching subset (`framingham.csv`)

## How to reproduce this analysis from scratch

1. Clone this repo:
   git clone https://github.com/niyyao/lab-2-framingham.git
   cd lab-2-framingham

2. Install the required Python packages:
   pip3 install pandas matplotlib jupyter

3. Launch Jupyter:
   jupyter notebook

4. In the browser tab that opens, navigate into the notebooks/ folder and
   open lab2_framingham.ipynb.

5. In the Jupyter menu, click: Kernel -> Restart & Run All
   (This re-fetches the dataset live from its source URL below, re-runs every
   cell in order, and regenerates the chart. An internet connection is required.)

6. Confirm it completes top-to-bottom with no errors and no manual steps.

## Data source

The dataset is not stored in this repo. It is loaded at runtime directly from
its original public source:

https://raw.githubusercontent.com/GauravPadawe/Framingham-Heart-Study/master/framingham.csv

This is a de-identified teaching subset of the Framingham Heart Study
(~4,000 rows, one row per participant, 10-year CHD outcome), not the
restricted-access NHLBI Framingham data.

## What the notebook does

- Loads the dataset from the URL above
- Bins participants into 4 age groups and labels smoking status
- Calculates observed 10-year CHD prevalence (%) by age group and smoking status
- Plots the result as a grouped bar chart
- Written interpretation of the pattern
