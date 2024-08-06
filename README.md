# deep-learning-challenge
UofU Data Analytics Module 21 Challenge

The "models" folder has the exported .k5 models themselves, and the "notebooks" folder has the code that produced them. The optimized versions are ones that I used to attempt a better model.

# 1.Overview:
    This analysis aims to discuss this model. In this scenario, we are looking at the nonprofit foundation Alphabet Soup's data on businesses and aims to predict whether or not they will be successful using binary classification. The model was created and trained off of csv files using tensor flow and was made with a goal of 75% accuracy.

## 2.Results:
### Data Preprocessing:
* The primary target variable was if the business would be successful or not depending on funding. 
* The features of this dataset were Affiliation, Classification, Organization, Use, Status, Income Amount, Ask Amount and Special Considerations; this is what the model was actually trained on.
* The Name and EIN number were removed from the input data simply because they are unique identifiers and do not participate in prediction

### Compiling, Training, and Evaluating the Model
* I ended up settling on 4 layers (including the input and output layer), and a neuron structure of 50-25-10-1. I tested multiple combinations, however this was the highest accuracy score I could achieve. I primarily used relu for the activation layer and sigmoid for the final output layer, but a tahn layer did increase the accuracy as well, so I threw that in as well.
* I was sadly not able to achieve the 75% threshold. Despite getting close, it seemed like most combinations did not point in the right direction.
* I took a few steps to increase model performance. At first, adding more layers seemed to up the accuracy, but in the end it actually lowered it. This is true as well for the amount of neurons in said layers; this suggests a bias or overfitting, so to remedy this, I lowered the amounts of neurons and layers. Epochs also seemed to contribute, and the healthiest balance between time and iterations was around 15-30. I'm sure that with more epochs, it would be able to self correct after some time, but the previously stated range put me close enough and didn't seem to affect performance too much.

# 3.Summary:
    Overall, the results are a bit disheartening, as 75% seemed to be within reach. I believe with the right combination it would be possible to hit this metric, however I think a better approach would be to try something else entirely. Perhaps a CNN model could perform better, and combine that with better scaled data, should show results. One could also limit the dataset to prevent bias, or split it differently.