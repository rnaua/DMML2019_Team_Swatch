# US Border Crossing Entries

## Team Swatch
---
* Tanja Markotic
* Arnaud Salvadori
* Yoann Petten
* Alvin Fournier

## Structure

The notebook were written considering people would pull the content of the git. The import was made with relative path. It would wiser to make this project run in local after downloading the needed datasets and notebooks.

### Data

In this project we will work on this dataset : "US borders crossing entries". This dataset comes from the US transportation department website : [https://data.transportation.gov/Research-and-Statistics/Border-Crossing-Entry-Data/keg4-3bc2/data]. It registers the inbound crossing at every port for the period of january 1996 to june 2019. Every port keeps track of the entries by registering the means of move of the crossing in the columns "Measure".

Here is a short explanation of the feature of this dataset :
* *Port Name* : Name of the port of entry
* *State* : The state in which the port is located
* *Port Code* : Identifier of the port, it is unique for each port
* *Border* : The border related to the port, either US-Canada or US-Mexico
* *Date* : Date of the recording
* *Measure* : Types of recordings, either the way of travelling or the type of merchandise
* *Value* : The number of crossing
* *Location* (added later) : The geographical coordinates of the port




The initial dataset is stored as `Border_Crossing_Entry_Data.zip` in the data folder. This will be the base for the cleaning work.

In the cleaning we will clean the data and augment the dataset with the locations of the different ports. The result dataframe is `DataWithLocationCleaned.csv.gz`. It will be used in the EDA and the Machine Learning part.

### Code

For more clarity and to avoid long charging time in our notebooks we decided to split it in three : 
1. Cleaning :
>In the notebook `Cleaning_Master` we clean our dataset and augment it with positions
2. EDA :
>In the `EDA` notebook we analyzed some potential issues with our data and made decisions to improve the quality of our predictions
3. Machine learning :
>In the `MachineLearning` notebook, we created several models that trained on a part of the data (train) and tested their efficacity on the other part of the dataset (test). The model we used are :
    * Logistic Regression
    * Linear Regression
    * Decision Tree
    * Random Forest
