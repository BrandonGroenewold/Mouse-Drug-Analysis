# matplotlib-challenge
Analyzing mouse data for testing on certain drugs.

## Skills/Languages used
- Jupyter Notebook, Python, MatPlotLib, Scipy, Duplicates Function, Drop Function, Loc Function

## Objective
- Generate all of the tables and figures needed for the technical report and to produce a top-level summary of the study results.

## Instructions

I will do the following:

* Prepare the data.

* Generate summary statistics.

* Create bar charts and pie charts.

* Calculate quartiles, find outliers, and create a box plot.

* Create a line plot and a scatter plot.

* Calculate correlation and regression. 

* Submit your final analysis. 

### Prepare the Data

1. Run the provided package dependency and data imports, and then merge the `mouse_metadata` and `study_results` DataFrames into a single DataFrame.

2. Display the number of unique mice IDs in the data, and then check for any mouse ID with duplicate time points. Display the data associated with that mouse ID, and then create a new DataFrame where this data is removed.

3. Display the updated number of unique mice IDs.

### Generate Summary Statistics

Create two summary statistics DataFrames:

    * For the first table, I use the `groupby` method to generate the mean, median, variance, standard deviation, and SEM of the tumor volume for each drug regimen. This resulted in five unique series objects. Combine these objects into a single summary statistics DataFrame.

    * For the second table, use the agg method to produce the same summary statistics table.

### Create Bar Charts and a Pie Charts

1. I generated two bar plots.

    * I created the first bar plot by using Pandas's `DataFrame.plot()` method.

    * I created the second bar plot by using Matplotlib's `pyplot` methods.

2. I generated two pie plots. Both plots should be identical and show the distribution of female or male mice in the study.
    * For the first pie plot I used Pandas's `DataFrame.plot()`.
    
    * For the second plot I used Matplotlib's `pyplot` method.

### Calculate Quartiles, Find Outliers, and Create a Box Plot 

1. I calculated the final tumor volume of each mouse across four of the most promising treatment regimens: Capomulin, Ramicane, Infubinol, and Ceftamin. Then, calculated the quartiles and IQR and determined if there are any potential outliers across all four treatment regimens.

    * Started by creating a grouped DataFrame that shows the last (greatest) time point for each mouse. Then merged this grouped DataFrame with the original cleaned DataFrame.

    * Next I created a list that holds the treatment names, as well as a second, empty list to hold the tumor volume data.

    * Then I looped through each drug in the treatment list, locating the rows in the merged DataFrame that correspond to each treatment. Also appended the resulting final tumor volumes for each drug to the empty list. 

    * Determined outliers by using the upper and lower bounds, and then printed the results.
    
2. Using Matplotlib, generated a box plot of the final tumor volume for all four treatment regimens. Highlighted any potential outliers in the plot by changing their color and style.

### Create a Line Plot and a Scatter Plot

1. I selected a mouse that was treated with Capomulin and generated a line plot of tumor volume vs. time point for that mouse.

2. Next I generate a scatter plot of tumor volume versus mouse weight for the Capomulin treatment regimen.

### Calculate Correlation and Regression

1. After that I calculate the correlation coefficient and linear regression model between mouse weight and average tumor volume for the Capomulin treatment. 

2. Finally, plotted the linear regression model on top of the previous scatter plot.

