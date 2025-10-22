# Education Inquiry - Socioeconomic Factors as Predictors for ACT Scores

> This project seeks to determine whether the socioeconomic variables unemployment rate, college attendance, marital status, income, free & reduced lunch qualification and teacher salary per pupil can accurately predict ACT scores in the United States. 

---

## Project Overview

This project combines three seperate data sets containing predictive socioeconomic variables that were fit using a series of linear regression modles. 


- **Objective:** Determine what combination of, if any, scoioeconomic varaibles can predict ACT scores for highschool students. 
- **Domain:** Education
- **Key Techniques:** Single and Multiple Linear Regression Modeling & Iterative Imputing. 

---

## Project Structure

```
├── data/                 # Raw and processed data
├── code/                 # Jupyter notebooks and Python scripts
├── reports/              # Generated reports and visualizations
├── requirements.txt      # Dependencies
└── README.md             # Project documentation
```

---

## Data

- **Source:** EdGap.org ((https://www.edgap.org/#5/39.795/-95.993))
- Variables Used From This Source
  	- id — originally “NCESSCH School ID”
	- percent_college — originally “CT Pct Adults with College Degree”
	- rate_unemployment — originally “CT Unemployment Rate”
	- percent_married — originally “CT Pct Childre In Married Couple Family”
	- median_income — originally “CT Median Household Income”
	- average_act — originally “School ACT average (or equivalent if SAT score)”
	- percent_lunch — originally “School Pct Free and Reduced Lunch”
- Primary Source for Socioeconomic Varibales & ACT Scores 

- **Source:** National Institute for Education Statistics ((https://ies.ed.gov/))
- Variables Used From This Source
	- year — originally “SCHOOL_YEAR”
	- id — originally “NCESSCH”
	- l_id — originally “LEAID”
	- state — originally “LSTATE”
	- zip_code — originally “LZIP”
	- school_type — originally “SCH_TYPE_TEXT”
	- school_level — originally “LEVEL”
	- charter — originally “CHARTER_TEXT”
- Primary Source for School Identifying Characteristics

- **Source:** National Institute for Education Statistics ((https://nces.ed.gov/ccd/elsi/tablegenerator.aspx))
- Variables Used From This Source
	- l_id — originally “Agency ID - NCES Assigned [District] Latest available year”
	- salary_pupil — originally “Total Current Expenditures - Salary (Z32) per Pupil (V33) [District Finance] 2016-17”
- Secondary Source for Socioeconimic Variable 

---

## Analysis

All analyses were conducted in JupyterLab using Python 3.11.3 with the Conda base kernel. Code was organized within a single notebook and should be run from top to bottom, running each modular cell in sequence.

---

## Results

It was determined that a Multiple Linear Regression (MLR) model could predict ACT scores with a high degree of relative accuracy (low mean absolute error), achieving predictions within approximately 1.1429 points of the observed values. However, it was also found that percent_lunch (School Percent Free and Reduced Lunch) alone could predict ACT scores within a 1.1690-point range, making it the preferred, and simplest, accurate modeling variable studied.

It is worth noting that other socioeconomic predictors, such as percent_college, rate_unemployment, percent_married, and salary_pupil, were all Census Tract or district-wide statistics. These variables represent averages across many individuals, potentially including those who do not attend the schools being studied. For this reason, we cannot be certain whether increasing the granularity of these predictors would improve the accuracy of the model.

---

## Authors

- Carter Ellis Webb - (https://github.com/EllisWebb)

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## Acknowledgements

- Tools/libraries used: pandas, numpy, matplotlib.pyplot, seaborn, plotly, scikit-learn, and statsmodels.
  
- Inspiration or collaborators: Inspiration came from courswork completed in DATA 5100 01 25FQ Foundations of Data Science, Seattle University; pursuant to the Master's of Science: Data Science diploma.
