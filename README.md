# Programming-for-Data-Analysis-Project

This project was completed by - Keith Ryan (G00387816@gmit.ie)

## Overview of the Dataset
The brief for this project is to create a simulated dataset using known properties and could be about whatever the student chose.

The idea for my project was to generate data for 500 Irish adult individuals defining their Gender, Age, Height, BMI Category and Weight.
I see Gender as being the most significant variable for this dataset as it plays the most significant role in each of the other variables

### Research and Approach
Please find more detail for this section throughout the markdown in the Jupyter notebook.

To understand the make up of the irish population I used 2016 (https://data.cso.ie/table/IH307) and 2019 (https://data.cso.ie/table/EY007) data from the Central Statistics Office of Ireland, which provided accurate figures for the percentage of the overall population that fall under different categories for Gender, Age and BMI Category.

For determining height I used information from OurWorldInData (https://ourworldindata.org/human-height), which verifies that height is normally distributed and gives the mean and standard deviation for heights across gender.

The general approach taken was to first determine gender for 500 individuals who's age was between 18 and 64, to get this information I use the data from the CSO to give the percentage of population female and male and using that as a probability to choose for any given indivudal their gender.

Similar approach was taken for Age, where I split the dataset into female and male datasets and then determine the percentage of that population at each age. Using this information then to loop through the 500 individuals with known gender's to then pick their age.

Height then is simply determined using an individuals gender using a normal distribution with different mean and standard deviations (taken from the OurWorlInData article linked above), here age is ignored as it is assumed that each of the individuals are fully grown adults.

Lastly BMI Category and Weight are two variables I have grouped together as I ended up needing to add BMI Category as a variable to assist in determining Weight, the reasoning for doing so was I couldn't find a good representative dataset for how weight is distributed across an adult population (studies and journal articles I could find were either specific to children, obesity or developing countries which would not have been representative for an Irish adult population, therefore I went with the best set of data which I could find around rates of BMI Categories across the Irish population).
BMI Category is based off the percentage of the population that falls under the categories of 'Under weight', 'Normal weight', 'Over weight' and 'Obese', and is similarly applied to how the Age variable was generated. Using then the generated value for BMI Category allowed me to set limits for an individual for what their BMI falls between and using a uniform distribution to pick out a BMI value between that range. Finally using that BMI value we can work back to a Weight by using the standard BMI formula as we have a value for BMI and height.


## Running the Notebook
The cells throughout this notebook go from beginning to end linearly, most of the work was done in figuring out appropriate ways to generate the data so the bulk of content can be found in markdown cells, relatively few lines of python code are needed to generate the data and much has been removed as the project developed.
There are two .csv files that the notebook requires (in the Data directory) in order to run as it performs some analysis on these files in order to get figures it needs for synthesizing the data.
If trying to run this notebook in a fresh environment the following packages will be required - pandas, numpy, matplotlib and seaborn.

## Results and Conclusions
I will briefly describe some conclusions here, but to see the proper results and conclusions I would recommend executing each of the cells in the notebook and reading through the markdown on observations and the approach as you go as all of the results and conclusions are contained therein. However it should still be relatively straightforward to follow without doing so and I have included a 'synthetic-adult-data.csv' file in the repository as an example of the generated data.

Overall I am pleased with the outcome of this project and have learned much in doing it and identified further areas to read up on and explore, especially in the areas where I feel my creating of fake data fell short.
To figure out what are sensible ways of making up the data I used data from multiple sources but primarily from the Central Statistics Office of Ireland, which gave me confidence that what I was generating was a good representation of the Irish population.
I am however uncofident of whether the choices made around generating weight are indeed a good representation, I believe it works well with the variables of Gender and Height and the resulting Scatterplot looks appropriate. However when Age is included against Weight, the data simply looks noisy which is a result of not factoring in age as being a variable impacting weight and were I to redo this project this would be one of the primary areas I would focus on so that each of the variables has a clear impact on weight - while working on this project it higlighted to me the importance of having multiple variables impact a single variable but at this stage in my understanding of Data Analysis I'm unable to reproduce this.

The potential use of a dataset such as this would be to provide data for individuals, while the Central Statistics Office provides great aggregated data, there are ocassions where having it non aggregated and based on individuals is very useful and so the ability to generate such a dataset based around these known properties has significant value to the scientific community for performing many different kinds of analysis.

