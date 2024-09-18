# How Important is the Serve in Tennis? (ATP Tour)
###### This project was completed as a requirement for the Data Analytics Program by CareerFoundry
## Project Overview
###### This project is intended to be used for fun only by general tennis fans who enjoy match analyses.
###### The serve is one of the most important strokes in tennis. The player who is serving usually has the advantage in a rally. Using data from the ATP Tour (professional men’s tennis), this project will explore three of the most common statistics, listed below, regarding the serve and their impact on the likelihood of winning a match:
### Serve Statistics
##### 1) Percentage of Points Won on First Serve
##### 2) Percentage of Points Won on Second Serve
##### 3) Percentage of First Serves in Play

###### This project will also explore how or if each of the three statistics varies between the three most commonly used court surfaces: grass, hard and clay.
###### Last, this project will explore the serve statistics of Roger Federer, Rafael Nadal and Novak Djokovic at three of the four Grand Slam Tournaments; Wimbledon, Roland Garros and the Australian Open. These three players are arguably the three greatest players of all time and collectively known as the “Big 3”. Each of them has the record number of titles at one of the aforementioned Grand Slams (Federer at Wimbledon, Nadal at Roland Garros and Djokovic at the Australian Open). Each of these slams is also played on one of the three aforementioned surfaces. Their serve statistics will then be compared to the average match winner, taking court surface into consideration.
### Project Questions:
##### 1) Of the three listed serve statistics, which has the greatest correlation with winning a tennis match on the ATP Tour?
##### 2) Did the impact of the most impactful serve stat (determined in question 1) change depending on the court surface?
##### 3) Novak Djokovic, Roger Federer and Rafael Nadal are collectively known as the BIg 3 and as of May 2024, they hold the record number of most Grand Slam Tournaments Won (Djokovic at 24, Nadal at 22, and Federer at 20). How did the Big 3’s serve statistics compare to average winners at their most successful Grand Slam Tournaments (which are the Australian Open, Wimbledon and Roland Garros, respectively)?

## Tools/Skills Used
##### Skills: Data Cleaning, Data Wrangling, Deriving New Variables, Project Designing, Logistic Regression, Data Visualization, Storytelling with Data
##### Tableau
##### Jupyter Notebooks
##### Python: pandas, numpy, os, matplotlib.pyplot, seaborn, scipy, sklearn.model_selection, sklearn.linear_model, sklearn.metrics, train_test_split, accuracy_score, confusion_matrix, classification_report

## Data

##### The original dataset contains the following data tables (there is also a folder containing unused JSON files that were not used for this project)

###### 1) matches
###### 2) players
###### 3) rankings

### Data Source and Content
###### “The data set contains the details about all the ATP matches played since 1968. The match statistics are available for matches since 1991.” This dataset is updated annually and also cites the following two credits: - <http://www.tennisabstract.com> - Jeff Sackman
###### Link to Data: Downloaded From: <https://www.kaggle.com/datasets/sijovm/atpdata/data>

## Link to Tableau Storyboard:

##### https://public.tableau.com/app/profile/tristan.savella/viz/CareerFoundry6_7/HowImportantistheServeinTennis?publish=yes

## Data Cleaning, Preparation and Wrangling

###### Only the "matches" dataframe was used for this project. 

##### Step 1. Data Cleaning and Prep
###### Removed data with missing match statistics (See Notebook 1a Section 3A) 
##### Step 2. Derived new variables 
###### Calculated the three serve statistics for this project for the winner and loser of each match (See Notebook 1a Section 3B)
##### Step 3. Data Cleaning 2
###### Removed data from before year 2000 (See Notebook 1a Section 3C)
##### Step 4. Create subsets of dataframe
###### Subsets according to court surface (grass, hard and clay courts - See Notebook 1b)
##### Step 5. Initial Exploration of Relationships between Variables
###### Explored relationships for main data frame and subsets, to get insights for each court surface (See Notebook 2)
##### Step 6. Data Wrangling for Logistic Regression 
###### Created dataframe consisting of each match winner and loser's serve stats, and a new variable: 1 = match winner; 0 = match loser (See Notebook 3a and 3b)

## Analysis and Insights

#### Initial Exploration

##### Using a correlation heat map, I observed any relationships between the variables. I found the following:
###### 1. Strong negative correlation between a match winner's %1st serve points won and number of break points he faced (-0.542)
###### 2. Moderate negative correlation between a match winner's %2nd serve points won and number of break points he faced (-0.435)
###### 3. No correlation between a match winner's %1st serves in play and number of break points he faced (-0.084)
##### Hypothesis: Of the three statistics, a player's %1st serve points won has the strongest correlation/impact to whether or not a player will win the match.

![Coefficient Serve Stats](Master%20Folder%20ATP/04%20Tableau/images/initial_correlations.png)

#### First Insights for Serve Stats by Court Surface 
###### 1. The winning players won a higher percentage of points behind their 1st serves on grass courts (78.7%), followed by hard courts (77.2%), then clay courts (73.6%); there is a noticeably wider gap between clay courts and the other two surfaces
###### 2. The winning players also won a higher percentage of points behind their 2nd serves on grass courts (56.9%), followed by hard courts (56.4%), then clay courts (55.8%).
###### 3. The winning player's % of 1st serve points won varied greater depending on court surface than % of points won on their 2nd serve.

![Coefficient Serve Stats](Master%20Folder%20ATP/04%20Tableau/images/serve_stats_by_surface.png)

#### Using the wrangled data frame (from Step 6 of Data Cleaning/Prep) and logistic regression, each of the three serve statistics were tested to see their correlation with the likelihood of winning a match on the ATP Tour. 

###### 4. The results indicate a weak correlation for both percentage of points won on first and second serve (0.15% and 0.10% respectively), and no correlation between a player's first serve percentage (0.04%).

![Coefficient Serve Stats](Master%20Folder%20ATP/04%20Tableau/images/coefficient_serve_stats.png)

#### The next step was to see if/how these correlation coefficients changed depending on court surface. 

###### 5. The correlation coefficients for all three serve statistics remained consistent across all three court surfaces
###### 6. Curiously, the correlation coefficient for points won behind a player's first serve was slighty higher on clay courts than the other two surfaces. This indicates that this statistic is equally important on clay courts despite player's winning the lowest percentage of first serve points on this surface

![Coefficient Serve Stats](Master%20Folder%20ATP/04%20Tableau/images/coefficient_serve_stats_surface.png)

##### Please see my Tableau Storyboard for more information regarding the "Big 3's" serve stats at their favorite slams.

## Further Recommendations

###### 1. Serve stats alone cannot explain match outcomes - other datasets may exist which contain additional statistics (groundstroke winners, unforced errors, etc.)
###### 2. Further exploration of which other elements are affected by court surface (use/effect of spin, rally length, etc.)
###### 3. Only one of the three dataframes were used for this project - the other two dataframes contain additional, potentially insightful variables for further research (such as player's heights or rankings)

## Conclusions

#### What I Learned
###### 1. This was my first experience designing my own project from a self-chosen dataset.
###### 2. Through this project, I practiced with deriving new variables in python, as the three serve statistics I wanted to explore were not in the original dataset
###### 3. This was my first experience using any form of regression analysis

#### Next Steps
###### 1. Consider using a linear regression for this analysis to see the relationship between serve statistics and the likelihood of winning match (rather than predicting a binary outcome as with logistic regression)
###### 2. The analysis included data from all ATP matches, regardless of if matches were played best of 3 or 5 sets. Grand Slams are in the minority of tournaments that use the best of 5 format. It may be interesting to consider it the average statistics or correlations are different between the two formats (Best of 3 or 5 sets).
###### 3. Match wins cannot be determined by serve alone - it would be useful to research the impact of other statistics (such as winners, unforced errors, etc.) and how these variables differ across court surfaces
###### 4. Only one of the three available data frames were used for this project - there is potential for further research by using the other available data in this set (such as the impact of a player’s height on serve, or the correlation between player rankings and serves, etc.)


## Folders

###### The following folders can be found in the master folder called, "Master Folder ATP"

#### 01 Project Overview

###### Project Overview

#### 02 Data

###### The original dataset and prepared/wrangled versions of the data

#### 03 Scripts

###### All executed codes divided by task objectives, including a folder of scripts that ended up being unused for the final presentation.

#### 04 Tableau

###### PDF of the Tableau Storyboard and an Outline of the Storyboard
