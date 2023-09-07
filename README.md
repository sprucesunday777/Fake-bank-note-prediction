Fake Bank Notes Detection
 


Introduction

The one important asset of a country is Bank currency.  Cash continues to play an important role in the economy as a medium of exchange and a store of value. To trade off goods and services, currencies are used all over the world. Since coins are difficult to pass, paper currency is increasingly becoming more common. People are enticed to copy original currencies as a result of this. Counterfeiting currency is a crime and is considered fraud – this is because counterfeits are worthless and victims cannot be reimbursed for their loss. The counterfeit banknotes detection and minimizing damage is one of the important elements. For cash to function effectively, however, it is important to maintain public confidence in the security of banknotes,  and to create discrepancies of money,  miscreants introduce fake notes which resemble the original note in the financial market.  Since there was no mechanism in place to recognize fake currency notes in the beginning, the supply of counterfeit currency notes grew day by day. Every country has its own currency. Size, form, color, and pattern are all different. It is tough to count various denominations and distinguish fake notes as all notes are subjected to mandatory testing. To overcome this issue, a currency recognition system is required in banking and other money transaction services. Automated teller machines, automatic good selling machines, and other similar machines are now commonly used in stores and bank counters. Currency recognition technology essentially seeks to recognize and extract visible and invisible features of currency banknotes. Several methods for identifying currency notes have been suggested up to this stage. However, the most effective method is to make use of the note's obvious features.

            Identification of counterfeit banknotes is done by using machine learning techniques. The method involves extracting and encoding various features to have a difference between fake and genuine banknotes using machine learning classification. The result of this process is used in validation and testing.

Problem Statement

This Project, sets to use supervised learning models which involves various classifier algorithms as a binary classifier that separates two classes, to disclose features that could identify if a banknote is counterfeit or original. 

Aim and Objectives

The objective of this project is to implement an efficient banknote detector system using machine learning classification, and a Web-based app for the user interface.This aims to identify banknote denomination and direction by features which will be carried out to derive useful information from the banknotes and finally using ML classification to identify features to recognize banknotes directions and classify banknotes into distinct denomination categories.
Specific objectives of this project seeks to:

➤ To collect dataset with various features of both genuine and counterfeit banknotes.
➤ To identify the best classification  model from existing models using the recommended algorithm for classification.
➤ Build and Train predictive model that can classify banknotes as real or counterfeit.
➤  To develop Web-based application (software) for user interface.

Significance of Project / Expected Outcome

This project will be useful for the banking sector in detecting the security features or characteristics of banknotes in order to determine whether any given banknote is counterfeit or genuine, and by so doing reducing the circulation of counterfeit banknotes in a country’s economy to stop inflation or any form of negative impact on the economy.  It could therefore, save individuals from not losing because counterfeits are worthless and victims cannot be reimbursed.



Dataset

The dataset used for this project was collected from Kaggle 
The link for the dataset:
https://www.kaggle.com/datasets/chrizzles/swiss-banknote-conterfeit-detection
The dataset includes information about the shape of the note, as well as the label. It is made up of 200 banknotes in total, 100 for genuine and counterfeit each, including various features like: length, left, right, bottom, top and diagonal and the target variable having two main values, genuine (label 0) and counterfeit (label 1) banknotes. Overall with data types: float64(6), int64(1).

Methodology

This project adopted the quantitative approach to data analysis in processing and analyzing the data. In other words, the data was handled by:

◼  Data collection: The team sourced secondary data from Kaggle as stated earlier. 
◼  Data cleaning: The dataset is rid of null values, special characters,white spaces in columns and in data.Since half of the data consist of outliers (counterfeit bills), so more robust methods will be needed.
◼  Data validation/evaluation: Seven (7) machine learning algorithms were then evaluated on the dataset using the f1 score, precision, recall and accuracy.

Data Visualization/Exploration(EDA)

With 6 measurements of banknotes given, which are:
Length
Right
Left
Top 
Bottom 
Diagonal
An exploratory data analysis was performed on some of the measurements above. Using seaborn countplot, showing the count of some features 

i) Diagonal measurements: As shown below, the bar chart shares insights on various diagonal measurement on how to identify if a banknote is genuine or counterfeit. The bar chart shows that the diagonal of genuine banknotes (0) has measurements from 140.6 - 142.4 with 141.5  having a count of 12 and 141.8 having a count of 11, these typically means that most genuine banknotes has diagonals of 141.5 - 141.8, while counterfeit banknotes (1) diagonal takes various measurements from 139.4 - 138.3  and 139.4, 139.2 and 139.6 having the highest count of 10, this means most counterfeit banknotes diagonal has those measurements.



ii) Left measurement: The bar chart below shows the left measurements for genuine banknotes (0) have a range of 129.9 - 130.7 as 129.9 and 129.7 having the highest counts, meaning that most genuine banknotes have those left measurements. Left measurements for Counterfeit banknotes (1) has ranges from 130.5 - 129.6 as 130.5, 130.4, 130.2 has the highest count of about 15, which means most left measurements of counterfeit banknotes has those ranges.


iii) Right measurements: 
The bar chart below shows a comparison between a genuine and fake banknote. Whereas right measurement for genuine notes (0) has a range of 129.7 - 131.1 as 129.7 having the highest counts of 16, it is obvious that most right measurements for genuine banknotes is 129.7. Right measurements for counterfeit notes (1) ranges from 130.3 - 129.6 as 130.3 and 130.4 has the highest count of 15, which means most right measurements for counterfeit notes is 130.3 or 130.4 . 


Data Preprocessing

The dataset do not have any missing values, so to proceed, finding outliers was a major step. The dataset having dependent variable (‘counterfeit’) columns and independent variables (length, left, right, bottom, top and diagonal) which are of both int and float d-types (numeric data), calculating the mean, median and mode of the entire dataset,was a vital step carried out to performing a statistical method on finding outliers. The box plot below also shows features that had outliers.



Checking for normality in the data, null hypothesis test was performed using shapiro library and an alpha level of 0.05 was chosen, 5 some features having a p-value of less than 0.05 were not normal. While handling outliers,  rescaling the data was the best option, because the dataset has less data points and in that case we can not afford to drop or mark the outliers. 



Model Implementation, Training and Evaluation

Lazy predict algorithm was used for different model performance testing 
Before training a model, a robust method of labeling and handling outliers, the InterQuartile Range(IQR) was used. All models had an of f1-score: 1.0, accuracy: 1.0, precision: 1.0 and a recall: 1.0, all except for label spreading classifier with an of accuracy: 0.9827.

Conclusion
In conclusion, a classification predictive system of fake banknotes detection can offer banks, local business owners and finance firms as an assisting tool. The system may be used to identify measurements and extract patterns to detect fake notes thereby reducing damage and loss to businesses and the economy at large.



