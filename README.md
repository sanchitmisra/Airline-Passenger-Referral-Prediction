# Airline-Passenger-Referral-Prediction
Capstone Project- Classification, Predicted if the passenger's recommend airline to his friends or not.

# Probelm statement:-

Data includes airline reviews from 2006 to 2019 for popular airlines around the world with
multiple choice and free text questions. Data is scraped in Spring 2019. The main objective
is to predict whether passengers will refer the airline to their friends.


## Feature descriptions briefly as follows:

**airline**: Name of the airline.

**overall**: Overall point is given to the trip between 1 to 10.

**author**: Author of the trip

**reviewdate**: Date of the Review customer review: Review of the customers in free text format

**aircraft**: Type of the aircraft

**travellertype**: Type of traveler (e.g. business, leisure)

**cabin**: Cabin at the flight date flown: Flight date

**seatcomfort**: Rated between 1-5

**cabin service**: Rated between 1-5

**foodbev**: Rated between 1-5 entertainment: Rated between 1-5

**groundservice**: Rated between 1-5

**valueformoney**: Rated between 1-5

**recommended**: Binary, target variable.

# Dataset
![1](https://user-images.githubusercontent.com/99437560/186843280-56c364af-0d76-48de-9fa0-c982982ce7eb.png)

# EDA
An EDA is a detailed analysis designed to reveal a data set's underlying structure. It is significant for a business because it identifies trends, patterns, and linkages that are not intuitively clear.

## Univariate Analysis:
 ## Numerical Features:
![image](https://user-images.githubusercontent.com/99437560/186843757-53d2901c-250f-407a-9d56-ce9cd6bb069e.png)![image](https://user-images.githubusercontent.com/99437560/186843881-a1fc7197-d398-45cd-a873-fc4e09fdc6a8.png)![image](https://user-images.githubusercontent.com/99437560/186844037-e35010b9-6455-4697-9526-8542e705583a.png)![image](https://user-images.githubusercontent.com/99437560/186844104-d60d2852-d11e-48c4-a40a-46d0a8543eda.png)![image](https://user-images.githubusercontent.com/99437560/186844164-dd331ff0-4267-4b54-9846-0296e3da9864.png)![image](https://user-images.githubusercontent.com/99437560/186844300-92c523f9-33f4-4f12-b69c-4a06907a82f7.png)![image](https://user-images.githubusercontent.com/99437560/186844439-ad42ccab-7509-42c8-bc19-033920aafd21.png)![image](https://user-images.githubusercontent.com/99437560/186844514-b4ebc823-80fd-47bc-994e-65040340d5e9.png)![image](https://user-images.githubusercontent.com/99437560/186844550-1fe57974-e0b6-4783-bec3-d7df61037665.png)
## Outlier Detection
![image](https://user-images.githubusercontent.com/99437560/186844908-f5ce50b5-7b74-4093-8059-1cd971bb9650.png)
Therefore, no outliers has been detected in dataset.
## Categorical Features:
The most frequent airline in the dataset, Spirit Airlines, maintains the top spot for the number of flights, followed by American and United airlines. As shown below:
![image](https://user-images.githubusercontent.com/99437560/186845049-34a40cfd-c7e7-47cf-8b5d-769e1a95a411.png)
The most frequent Aircraft in the dataset, Airbus A320, maintains the top spot for the number of flights, followed by Boeing 777  and Airbus A380 aircraft.
![image](https://user-images.githubusercontent.com/99437560/186845468-b559d7ce-cff3-4bd3-9859-95fa2c0f7498.png)
According to the above analysis, Bangkok to Hong Kong journey with maximum frequency in dataset holds the tops position followed by Bangkok to London and London to New York.
![image](https://user-images.githubusercontent.com/99437560/186845681-fa0d9eb7-c2a4-4e35-9feb-2d8dbec26976.png)
The month of July is said to be the one with the highest travel. The second-most popular month for travel is December.
![image](https://user-images.githubusercontent.com/99437560/186845776-059ce278-e130-44bf-b636-7d7040304df4.png)
The three plots mentioned above made it easier for us to understand that the majority of travellers are Solo Leisure in travellers type column.
For most passengers, the Economy class is the one they like in the cabin column.
There is slight variation between recommended and not recommended in the recommended column.
![image](https://user-images.githubusercontent.com/99437560/186845973-f5dbe2cc-f0f9-439b-8134-feed97b66460.png)![image](https://user-images.githubusercontent.com/99437560/186846051-c301b56a-1665-4dee-bed5-1ff7bff8f2b4.png)![image](https://user-images.githubusercontent.com/99437560/186846089-20f1b361-a363-4e50-b23e-28f0287d180d.png)
## Bivariate Analysis**:
All types of travellers strongly prefer the economy class.
Some of the Business class and Couple Leisure people choose business class for travelling.
First class is least preferred among all traveller type categories.
![image](https://user-images.githubusercontent.com/99437560/186846187-6f6c33df-1af8-4315-9c47-1e80e0f928be.png)
## Multivariate Analysis:
Airlines recent 5 year trend:
![image](https://user-images.githubusercontent.com/99437560/186846435-0306e333-513d-4567-888d-5d9cd0f04f40.png)
#**Multicollinearity**:
We can observe that a lot of rating variables have strongly correlated with the overall rating column. Therefore, we may ignore the remaining correlated columns and focus just on the overall column in order to optimize our analysis.
![image](https://user-images.githubusercontent.com/99437560/186846695-35a4f38b-b1c5-498d-9b1d-e46c84c6e270.png)
# Natural Language Processing:
##**Text Cleaning**:
Text cleaning is the process of preparing raw text for NLP (Natural Language Processing) so that machines can understand human language.
Following approach is used here to clean the text of customer reviews:
* **Use pos_tag with nltk**:- POS Tagging in NLTK is a process to mark up the words in text format for a particular part of a speech based on its definition and context. 
* Remove all character which are excluded from "**a-z and A-Z**".
* Convert words into **Lowercase** and **split** them through space.
* Remove **stopwords** using **nltk** library.
* Lemmatization of reviews and get the meaningful words using **WordNetLemmatizer**.
* **Join** back the words that were split before.
* Initiate **tokenization** process.
![2](https://user-images.githubusercontent.com/99437560/186847387-5fb6d82b-153c-460b-b434-c48b25df947f.png)
## Most Frequent words in customer review column:
![image](https://user-images.githubusercontent.com/99437560/186847481-2a27ed96-1654-4e19-a23e-44511fcf0679.png)
# Model performance:
![3](https://user-images.githubusercontent.com/99437560/186847845-7d988377-8d0c-4ef1-acdf-bdaaa0651689.png)
## Confusion matrix of test data
![4](https://user-images.githubusercontent.com/99437560/186848170-df2e6fb2-823a-4180-9e49-90d544d30077.png)
## Auc-Roc Curve:
![image](https://user-images.githubusercontent.com/99437560/186848344-319e7f1e-a580-4fc9-8341-5317da867f76.png)
# Model performance based on randomly created reviews:
![5](https://user-images.githubusercontent.com/99437560/186848578-0f82593a-09de-4710-bc74-02d432262394.png)
# Finally, interpreting the model through SHAP:
![image](https://user-images.githubusercontent.com/99437560/186848760-3df86158-934d-4be5-9280-55427bf0578c.png)
# Conclusion:
Logistic Regression performed best among all other algorithms for this particular type of dataset.
