# How Important is the Serve in Tennis? (ATP Tour)
###### This project was completed as a requirement for the Data Analytics Program by CareerFoundry
## Project Overview
This project is intended to be used for fun only by general tennis fans who enjoy match analyses.
The serve is one of the most important strokes in tennis. The player who is serving usually has the advantage in a rally. Using data from the ATP Tour (professional men’s tennis), this project will explore three of the most common statistics, listed below, regarding the serve and their impact on the likelihood of winning a match:
### Serve Statistics
##### 1) Percentage of Points Won on First Serve
##### 2) Percentage of Points Won on Second Serve
##### 3) Percentage of First Serves in Play
This project will also explore how or if each of the three statistics varies between the three most commonly used court surfaces: grass, hard and clay.
Last, this project will explore the serve statistics of Roger Federer, Rafael Nadal and Novak Djokovic at three of the four Grand Slam Tournaments; Wimbledon, Roland Garros and the Australian Open. These three players are arguably the three greatest players of all time and collectively known as the “Big 3”. Each of them has the record number of titles at one of the aforementioned Grand Slams (Federer at Wimbledon, Nadal at Roland Garros and Djokovic at the Australian Open). Each of these slams is also played on one of the three aforementioned surfaces. Their serve statistics will then be compared to the average match winner, taking court surface into consideration.
### Project Questions:
##### 1) Of the three listed serve statistics, which has the greatest impact on the likelihood of winning a tennis match on the ATP Tour?
##### 2) Did the impact of the most impactful serve stat (determined in question 1) change depending on the court surface?
##### 3) Novak Djokovic, Roger Federer and Rafael Nadal are collectively known as the BIg 3 and as of May 2024, they hold the record number of most Grand Slam Tournaments Won (Djokovic at 24, Nadal at 22, and Federer at 20). How did the Big 3’s serve statistics compare to average winners at their most successful Grand Slam Tournaments (which are the Australian Open, Wimbledon and Roland Garros, respectively)?

## Data

The original dataset contains the following data tables (there is also a folder containing unused JSON files that were not used for this project)
##### 1) matches
##### 2) players
##### 3) rankings

### Data Source and Content
“The data set contains the details about all the ATP matches played since 1968. The match statistics are available for matches since 1991.”
This dataset is updated annually and also cites the following two credits: - <http://www.tennisabstract.com>
- Jeff Sackman
Link to Data
Downloaded From: <https://www.kaggle.com/datasets/sijovm/atpdata/data>

## Data Cleaning and Preparation

###### Only the "matches" dataframe was used for this project. The following steps were performed and can be viewed in Notebook 1a. "ATP Initial Exploration Part 1"
#### Step 1. Renamed variables (See Section 3A in Notebok 1a.)
#### Step 2. Derived new variables - calculated the three serve statistics for this project for the winner and loser of each match (two of the three serve statistics - See Section 3B in Notebook 1a)
#### Step 3. Remove all data for matches played before the year 2000 (See Section 3C in Notebook 1a.)

## Analysis and Insights

## Link to Final Presentation on Tableau Public:

https://public.tableau.com/app/profile/tristan.savella/viz/CareerFoundry6_7/HowImportantistheServeinTennis?publish=yes

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

## Tools Used
###### Tableau
###### Jupyter Notebooks
###### Libraries (pandas, numpy, os, matplotlib.pyplot, seaborn, scipy, sklearn.model_selection, sklearn.linear_model, sklearn.metrics, train_test_split, accuracy_score, confusion_matrix, classification_report, LogisticRegession)
