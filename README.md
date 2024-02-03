This project is based on "The Complete Pandas Bootcamp 2023 - Data Science with Python," a course offered by Udemy and taught by Alexander Hagmann. It presents a Data Aggregation challenge, requiring the application and combination of various concepts and methods.

This project is focuses on Exploratory Data analysis (EDA). EDA is a crucial step in the data analysis process that 
involves summarizing, visualizing, and understanding the main characteristics and patterns within a dataset. 
The primary objectives of EDA in this project:

**Data Inspection:**
- Import the Datasets Summer (summer.csv), Winter (winter.csv) and dictionary (dictionary.csv) and Inspect!

**Merge and Concatenate:**
1. Merge Summer and Winter (one row for each Medal awarded in any Olympic Games) and save the merged DataFrame in olympics.
2. An additional column (e.g. "Edition") shall indicate the Edition -> Summer or Winter.
3. Add the full Country name from dictionary to olympics (e.g. France for FRA).

**Data Cleaning:** 
1. Remove Spaces from column headers in dictionary. 
2. For some Country Codes, there is no corresponding full Country Name available (e.g. for "URS") -> missing values
in olympics. Identify these Country Codes and search the Web for the full Country Names. Replace missing values in 
Country column!
3. Remove rows from olympics where the Country code is unknown. (Make sure you reset the Index -> RangeIndex)
4. Convert the column Medal into an ordered Categorical column ("Bronze" < "Silver" < "Gold")

**Exploratory Data Analysis** 

- **Do GDP, Population and Politics matter?**:
  1. Create the following aggregated and merged DataFrame with Top 50 Countries (you can see an excerpt with the first
  12 Countries). The Column Total_Games shows the number of Participation (as an approximation: determine the number of
  Editions where Countries have won at least one medal).
  2. Convert the absolute values in the DataFrame into ranks and save the ranks DataFrame in new variable
  (see screenshot). Ranks are more meaningful than absolute numbers.

- **Statistical Analysis and Hypothesis Testing with scipy:**
  In the following work with Ranks! Check whether GDP (Standard of Living), Total_Games (Political Stability measure)
  and Population (Size) have an effect on Total Medals. (hint: work with spearman correlation, not with pearson 
  correlation). In this part, we are going to test whether the factors population, GDP per capita and the number of
  participation influence and determine a country's success in Olympic Games with statistical significance.

- **Medals Heatmap by Gender and Edition:**
  Create the following Seaborn Heatmap with Medal Ranks for Top 50 Countries (Total Medals, Summer Games Medals,
Winter Games Medals, Men, Women).

- **Summer Games vs. Winter Games - does Geographical Location matter?:**
Identify Countries that are 
* equally successful in Summer and Winter Games 
* more successful in Summer Games 
* more successful in Winter Games
What could be the reasons?
1) First, let's compare summer athletes to winter athletes in the same country, who got more medals. Identify
countries where athletes got more medals in the Winter Games than in the Summer Games and vise verse
2) Second, lets compare athletes in summer games in one country to athletes in summer games in another country.
In which countries the athletes got most medals. The same do for the winter games.

- **Men vs. Women - does Culture & Religion matter? :**
Identify Countries where
* Men and Women are equally successful
* Men are more successful
* Women are more successful
What could be the reasons?
1) First, compare men to women in the same country and who got more medals. Identify countries where the men got more
medals compared to women and identify countries where the women got more medals compared to men in the same country.
2) Second, we can compare the men in one country to the men in another country. In which countries the men got the
most medals. In which countries the men got the least medals. Identify those countries. Then, we can compare the women
in one country to the women in another country. In which countries the women got the most medals. In which countries 
the women got the least medals? Identify those countries.

- **Do Traditions matter?:**
Create the following Seaborn Heatmap that shows the Ranks of Top 50 Countries by Sports.
Identify traditional Sports / National Sports for e.g. UK and China!