# Programming-for-Data-Analysis-Project

This project was completed by - Keith Ryan (G00387816@gmit.ie)

## Overview of the Dataset
The brief for this project is to create a simulated datasetusing known properties and could be about whatever the student chose.

The idea for my project was to generate data for 500 Irish adult individuals defining their Gender, Age, Height, BMI Category and Weight.
I see Gender as being the most significant variable for this dataset as it plays the most significant role in each of the other variables

### Research
To understand the make up of the irish population I used 2016 (https://data.cso.ie/table/IH307) and 2019 (https://data.cso.ie/table/EY007) data from the Central Statistics Office of Ireland, which provided accurate figures for the percentage of the overall population that fall under different categories for Gender, Age and BMI Category.

For determining height I used information from OurWorldInData (https://ourworldindata.org/human-height), which verifies that height is normally distributed and gives the mean and standard deviation for heights across gender.

## Running the Notebook
The cells throughout this notebook go from beginning to end linearly, most of the work was done in figuring out appropriate ways to generate the data so the bulk of content can be found in markdown cells, relatively few lines of python code are needed to generate the data and much has been removed as the project developed.
There are two .csv files that the notebook requires (in the Data directory) in order to run as it performs some analysis on these files in order to get figures it needs for synthesizing the data.
If trying to run this notebook in a fresh environment the following packages will be required - pandas, numpy, matplotlib and seaborn.

## Results and Conclusions
To see the proper results and conclusions I would recommend executing each of the cells in the notebook and reading through the markdown on observations and the approach as you go as all of the results and conclusions are contained therein. However it should still be relatively straightforward to follow without doing so and I have included a 'synthetic-adult-data.csv' file in the repository as an example of the generated data.


