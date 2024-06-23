<!-- Improved compatibility of back to top link: See: https://github.com/othneildrew/Best-README-Template/pull/73 -->
<a name="readme-top"></a>
<!--
*** Thanks for checking out the Best-README-Template. If you have a suggestion
*** that would make this better, please fork the repo and create a pull request
*** or simply open an issue with the tag "enhancement".
*** Don't forget to give the project a star!
*** Thanks again! Now go create something AMAZING! :D
-->



<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->



## Titanic Logistic Regression<br>

Logistic regression is a statistical model used for binary classification tasks, making it particularly suitable for predicting outcomes with two possible values, such as whether a passenger survived or not in the Titanic dataset. In this context, the model learns a relationship between input features (e.g., age, gender, ticket class) and the probability that a passenger survived the Titanic disaster. The logistic regression model outputs probabilities between 0 and 1, representing the likelihood of survival. It achieves this by applying a logistic function to a linear combination of the input features. During training, the model adjusts its parameters to minimize the binary cross-entropy loss, which penalizes predictions that diverge from the actual survival outcomes in the training data. By training on historical data where survival outcomes are known, logistic regression learns patterns and correlations in the dataset. These patterns allow it to generalize to new, unseen data, predicting whether a passenger would have survived based on their characteristics.<br>

### Data<br>

The sinking of the Titanic is one of the most infamous shipwrecks in history. On April 15, 1912, during her maiden voyage, the widely considered "unsinkable" RMS Titanic sank after colliding with an iceberg. Unfortunately, there weren’t enough lifeboats for everyone onboard, resulting in the death of 1502 out of 2224 passengers and crew. While there was some element of luck involved in surviving, it seems some groups of people were more likely to survive than others.<br>

Download the dataset from [Kaggle Titanic Dataset](https://www.kaggle.com/c/titanic/data).<br>

## Steps <br>

### 1) Preparing Data <br>

To prepare the Titanic dataset for modeling, we performed the following steps:<br>
* Loaded the dataset.<br>
* Conducted exploratory data analysis (EDA) to understand the distribution and relationships among variables.<br>
* Handled missing values.<br>
* Converted categorical features into numerical representations using one-hot encoding.<br>
* Removed unnecessary columns that were deemed irrelevant for our analysis.<br>
* Ensured all numerical features were appropriately scaled for model training.<br>

### 2) Splitting the Data<br>

We split the preprocessed dataset into training and testing sets to evaluate the model's performance:<br>
- Divide the data into 80% training and 20% testing sets.<br>

### 3) Using Logistic Regression Model<br>

For predicting survival on the Titanic, we implemented a logistic regression model using PyTorch:<br>
- Defined a custom class in PyTorch.<br>
- Configured the model with four fully connected layers (64, 32, 16, 1) and ReLU activations, followed by a sigmoid activation at the output layer.<br>
- Utilized binary cross-entropy loss as the criterion for training the model.<br>
- Employed stochastic gradient descent (SGD) optimizer with a learning rate of 0.01 to minimize the loss function.<br>

### 4) Model Validation<br>

To validate the performance of our logistic regression model:<br>
- Evaluated the model's accuracy and loss on the validation set during training to monitor its learning progress.<br>
- Tested the model's predictive capabilities on unseen data from the testing set to assess its generalization ability.<br>
- Demonstrated model validation by selecting a random passenger example from the dataset, inputting their features into the trained model, and interpreting the predicted survival probability.<br>



### Dependencies<br>

- numpy<br>
- pandas<br>
- seaborn<br>
- scikit-learn<br>
- matplotlib<br>
- torch<br>
