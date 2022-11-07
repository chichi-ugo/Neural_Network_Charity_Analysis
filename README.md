# Neural_Network_Charity_Analysis
Using Machine Learning and Neural Networks to predict successful charity funding

## Purpose and Overview
In this project we used Sckit-learn and Tensorflow to develop machine learning models - specifically deep neural network model. We aim to compare the differnce between neural models and deep neural models, implement the models, and save the outputs.

The goal of this analysis is to create a classifier to predict the success of charities funded by the AlphabetSoup company. We used a dataset containing features of the company's donations and trained the algorithm to identify successful vs. failed donations.

## Results
### Data Preprocessing
<!---What variable(s) are considered the target(s) for your model?-->
In the dataset provided, the column labeled "IS_SUCCESSFUL" was made the target for our model. This column indicates successful donations with a 1 and failed ones with a 0. 

<!---What variable(s) are considered to be the features for your model?-->
As for the features, These were defined as the following columns:

- APPLICATION_TYPE
- AFFILIATION
- CLASSIFICATION
- USE_CASE
- ORGANIZATION
- STATUS *
- INCOME_AMT
- SPECIAL_CONSIDERATIONS
- ASK_AMT     

<!---What variable(s) are neither targets nor features, and should be removed from the input data?-->
Initially, we dropped only the "EIN" and "NAME" columns. Later in the analysis, however, we also dropped the "STATUS" column as well (hence the astrisk above).

### Compiling, Training, and Evaluating the Model
<!---How many neurons, layers, and activation functions did you select for your neural network model, and why?-->
After multiple attempts in optimizing the model, we ended with 3 hidden layers with 100 neurons on layer 1, 60 on layer 2, and 40 on layer 3. We initially tested the ReLU functions, but then also tested the Tanh function as well.

<!---Were you able to achieve the target model performance?-->
Even after many iterations, we were unable to produce a model with a 75% accuracy rate.
<!---What steps did you take to try and increase model performance?-->
In attempts to increased model performance, we rebinned many of the feature variables into smaller number of groups. We also altered the "ASK_AMT" column in order to organize it into bins as well and binary incode it aswell. We dropped the "STATUS" column because upon looking at the values we sall that there were only 5 rows that held a 0 - not giving us very much information/variation. Lastly, we tried increasing the number of hidden layers and the number of neurons on each layer, as well as changing the activation functions for the layers.

## Summary
