# [Try Advertisement Click Prediction AI](http://ad-click-prediction-4.bubbleapps.io)

Targeting the right audience is a challenge in online marketing. Without knowing right audience to your products, you not only waste millions of dollars to display the advertisement to wrong audience, but also waste a lot of time to find right audience. To save marketing budget and time, I developed Advertisement Click Prediction with Peltarion and Bubble.
Advertisement Click Prediction predicts whether your advertisement will be clicked or not by your targeted audience. This app also predicts who will be your target audience. To predict advertisement clicks, you need to type following information: your target audience's age, gender, expected annual income, daily time spent on site, daily internet usage, and advertisement phrase. After typing all the information and clicking 'Predict' button, you will know whether your advertisement will be clicked or not.





# [Data](https://www.kaggle.com/kevinhartman0/advertisement-transcripts-from-various-industries?select=Advertisement_Transcripts_deduped_edited.xlsx)
### Data type: tabular (text, number)

The data consists of 10 variables: 
- Daily Time Spent on Site
- Age
- Area Income
- Daily Internet Usage
- Ad Topic Line
- City
- Male
- Country
- Timestamp
- Clicked on Ad


Each variable contains 1000 elements with no missing values within them.

### Briefly. I will describe variables:
- Area Income Variable: The smallest area income is $13,996.50 and the highest is $79,484.80. This means that site visitors are people belonging to different social classes.

- Daily Spent on Site Variable: Users spend between 32 and 91 minutes on the website in one session.  
- The average age of a visitor is 36 years. The youngest user has 19 and the oldest is 61 years old.   
- Male Variable: Women(52%) and men(48%) are almost equally visited. 

### To allow a machine learning model to establish valuable relationships and to improve the accuracy of the machine learning model, I excluded the following variables: 

- City Variable: 969 unique values out of 1000. Too many unique elements can cause difficult to perform a prediction. Because of that, city variable was omitted.  
- Country Variable: there are 237 different unique countries in the dataset and no single country is too dominant. A large number of unique elements hinder machine learning model to establish easily valuable relationships. For that reason, this variable was excluded.
- Timestamp Variable: All values are unique. this variable was excluded.  


### Data Description: 
This data set contains the following features:

- Daily Time Spent on Site: consumer time on site in minutes
- Age: cutomer age in years
- Area Income: Avg. Income of geographical area of consumer
- Daily Internet Usage: Avg. minutes a day consumer is on the internet
- Ad Topic Line: Headline of the advertisement
- City: City of consumer
- Male: Whether or not consumer was male
- Country: Country of consumer
- Timestamp: Time at which consumer clicked on Ad or closed window
- Clicked on Ad: 0 or 1 indicated clicking on Ad


### AI model description:
The model was built on the [Peltarion](https://peltarion.com/).  
1. I used **tabular binary classification** to classify advertisements that will be clicked or will not be clicked. 
2. Once the data was uploaded onto the platform, the **Tabular Binary Classification** snippet was chosen. 
3. Since all inputs need the same dimensionality, I added **BERT Tokenizer** and **English BERT encoder** under the 'Ad topic line' feature input that is consists of texts. BERT Tokenizer converts plain text into a sequence of numerical values.
4. To find out a feature that increases the accuracy of the model, I tested by excluding certain features. For example, I excluded the 'Daily Internet Usage' feature to see how the accuracy of the model changes. The accuracy of the model without the 'Daily Internet Usage' feature showed lower accuracy(76%) compared to the accuracy(100%) of the model that includes the 'Daily Internet Usage' feature.

### AI model accuracy:
The best model showed 100% accuracy in validation, 96% accuracy in training.
The model showed 100% Validation accuracy, 96% Training accuracy. Validation Loss is less than Training Loss.




