1. Data Cleaning
•	Convert Data Types: The columns "Rating" and "Number of Votes" were converted from object to numeric types to handle data properly in analysis.
•	Handling Missing Values:
o	Missing values in the "Rating" and "Number of Votes" columns were filled with their respective median values.
•	Drop Unnecessary Columns:
o	The "Index" column was removed if it existed, as it was redundant for our analysis.
2. Data Visualization Before Normalization
•	Distribution Plots:
o	Visualized the distributions of "Rating" and "Number of Votes" using histograms and Kernel Density Estimation (KDE) plots to understand their initial range and patterns.
o	This helped identify skewness, trends, or unusual data behavior before applying any transformation.
3. Data Transformation (Manual Normalization)
•	Manual Min-Max Normalization:
o	Normalized the "Rating" and "Number of Votes" columns using the formula:
arduino
Copy code
(value - min) / (max - min)
o	This scaled the values to a range between 0 and 1, making the features comparable and suitable for various machine learning models.
4. Data Visualization After Normalization
•	Post-Transformation Visualization:
o	Re-plotted the distributions of "Rating" and "Number of Votes" to observe how the data behaved after normalization.
o	These visualizations confirmed that the values were now standardized, with a consistent range.
5. Feature Engineering
•	Creating New Features:
o	Added a new column called "Author Book Count", which indicates how many times each author appears in the dataset.
o	This feature can be useful to gauge the popularity or influence of certain authors.
6. Data Reduction
•	Remove Less Useful Columns:
o	The "Score" column was removed to simplify the dataset, as it was deemed less useful for the analysis.
7. Outlier Detection
•	Detecting Outliers in Ratings:
o	Applied the Interquartile Range (IQR) method to identify outliers in the "Rating" column.
o	Calculated the IQR and set boundaries using the following formulas:
java
Copy code
Lower Bound = Q1 - 1.5 * IQR
Upper Bound = Q3 + 1.5 * IQR
o	Added a new column "Outlier_Rating" to mark rows with True if they were identified as outliers.
Key Points
•	Data Cleaning and Normalization: Ensured data consistency and prepared it for analysis.
•	Visualization: Provided insights into data distribution both before and after normalization.
•	Feature Engineering: Enhanced the dataset with a new, informative feature.
•	Outlier Detection: Identified and marked data points that deviate significantly from the norm.
