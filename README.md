# Disaster_or_not

Twitter has become an important communication channel in times of emergency.
The ubiquitousness of smartphones enables people to announce an emergency they’re observing in real-time. Because of this, more agencies are interested in programatically monitoring Twitter (i.e. disaster relief organizations and news agencies).

But, it’s not always clear whether a person’s words are actually announcing a disaster.




The following features with total of 8693 entries were provided in the train.csv i.e training set
 
 #   Columns/Features
 
 0   id
 
 1   keyword
 
 2   location
 
 3   text
 
 4   target
 
 


  


 #   Data Cleaning/Feature Engineering
 
 Train .fillna("") with empty string was done to training set to remove null values.
 
 Except 'Id' and 'Target' rest all have been combined together as a new feature= 'text_merged'  which will be used as single feature training set in a simplified way.
 
 then we clean the feature from punctuations and stopwords with stopwords from nltk.corpus library
 
 Then Tfidf Vectorization is done on this feature

We take 'Target' as our label ( train y) & 'text_merged' as our (train X) 
 

#   Machine Learning (Training the model)
Imported almost all the popular Classifier Algorithms

test_size was taken as 30%

The accuracy scores were computed as below
![image](https://user-images.githubusercontent.com/26757681/202672101-4f9abfa9-4c0a-42a4-9a58-b8c27cdeee72.png)
![image](https://user-images.githubusercontent.com/26757681/202671940-a7eecd19-25ce-449e-b055-afa10c159197.png)

The top three that is  LOG,MNB & SGD were applied on the test dataset and submitted on Kaggle for scores 

LOG submission scored slightly better compared to the other two 

Then did Hyper parameter tuning using Grid_Search_CV on LOG model then applied it on the test dataset and submitted on Kaggle for scores

  Accuracy_score= 0.79098
  My best on Kaggle so far and ranking is 464/871  that is top 54 of the total submissions on kaggle for this competiton.
  Will update improved results on this
