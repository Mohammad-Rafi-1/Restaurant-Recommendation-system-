# Restaurant-Recommendation-system-

The purpose of recommender systems is to make suggestions for products and concepts that fit a user's particular way of thinking.
Every day, data is generated in excess of 2.5 quintillion bytes (2.5 e+9 GB).
Recommender systems attempt to automate elements of an entirely different information discovery model in which users seek out others who share their interests and request their recommendations for new items.

<img src="https://user-images.githubusercontent.com/97906845/210183234-e31ade35-cc6d-4fc9-a5a4-ef36a3521afc.png" width=600>

# Dataset 

Dataset is collected from yelp website . The size of the datase is more than 2GB and it has following files

1) bussiness.json

2) reviews.json

3) Tips.json

4) users.json

The data: https://www.yelp.com/dataset

Please read about the dataset here: https://www.yelp.com/dataset/documentation/main 

# Exploratory Data Analysis

<img src="https://user-images.githubusercontent.com/97906845/210183175-c23e1ad5-7888-4045-871c-a5aeb7facd83.png" width=600>


you can check the complete data analysis of yelp dataset in file EDA_yelp_final.ipynb

# Matrix Factorization (Intuition behind recommendation system)

### Frist we will create adjacency matrix which consist's of user and restuarant information


<img src="https://user-images.githubusercontent.com/97906845/210187294-c46a9b15-f1bb-44a6-80c9-a76d105703e1.png" width=800>


### then we represent the matrix into product of Matrix (using sigular value decomposition)

<img src="https://user-images.githubusercontent.com/97906845/210187372-8c575d06-81c5-483a-8bda-c0c6a8bbea3e.png" width=800>


### From this we can capture the user and restuarant Latent vectors 

### we can use these vectors to find similar user or restaurants


### To capture the user bias and restuarant bias we post this as optimization problem as below

<img src="https://user-images.githubusercontent.com/97906845/210187484-0bd968e8-1624-4572-bcfd-c3301c7bf4f5.png" width=800>


### and we try to solve this problem by using regular optimization algorithms like SGD 

### after solving this we get user bias and restuarant bias , we can use this extra information to recommend restuarant to the user

### we can achieve the same approch both using Deep Learning and classical Machine Learning for more information look at the Model_building.ipynb file


