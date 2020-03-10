# Starbucks Capstone Project
This is my Starbucks Capstone Project for the Udacity Machine Learning Engineer Nanodegree. Udacity partnered with Starbucks to provide a real-world business problem and simulated data mimicking their customer behavior.

# Context
Starbucks Corporation is an American coffee company and operates over 30,000 locations worldwide. Once every few days, Starbucks sends out an offer to users of the mobile app. An offer can be merely an advertisement for a drink or an actual offer such as a discount or BOGO (buy one get one free). Some users might not receive any offer during certain weeks. The company would like to select customers with the highest probability of making a purchase, in contrast, want to know the customers who don’t like to receive offers too. In other words, the right offer to the right customer.

# Dataset
##### Dataset overview:
* The program used to create the data simulates how people make purchasing decisions and how those decisions are influenced by promotional offers.
* Each person in the simulation has some hidden traits that influence their purchasing patterns and are associated with their observable traits. People produce various events, including receiving offers, opening offers, and making purchases.
* As a simplification, there are no explicit products to track. Only the amounts of each transaction or offer are recorded.
* There are three types of offers that can be sent: buy-one-get-one (BOGO), discount, and informational. In a BOGO offer, a user needs to spend a certain amount to get a reward equal to that threshold amount. In a discount, a user gains a reward equal to a fraction of the amount spent. In an informational offer, there is no reward, but neither is there a requisite amount that the user is expected to spend. Offers can be delivered via multiple channels.
* The basic task is to use the data to identify which groups of people are most responsive to each type of offer, and how best to present each type of offer.

This is the data dictionary:

* Profile.json: Rewards program users (17000 users x 5 fields)
    * gender: (categorical) M, F, O, or null
    * age: (numeric) missing value encoded as 118
    * id: (string/hash)
    * became_member_on: (date) format YYYYMMDD
    * income: (numeric)
    
* Portfolio.json: Offers sent during 30-day test period (10 offers x 6 fields)
    * reward: (numeric) money awarded for the amount spent
    * channels: (list) web, email, mobile, social
    * difficulty: (numeric) money required to be spent to receive reward
    * duration: (numeric) time for offer to be open, in days
    * offer_type: (string) bogo, discount, informational
    * id: (string/hash)

* Transcript.json: Event log (306648 events x 4 fields)
    * person: (string/hash)
    * event: (string) offer received, offer viewed, transaction, offer completed
    * value: (dictionary) different values depending on event type
        * offer id: (string/hash) not associated with any "transaction"
        * amount: (numeric) money spent in "transaction"
        * reward: (numeric) money gained from "offer completed"
    * time: (numeric) hours after start of test

# Files
* **data/portfolio.json** - This was provided by Starbucks and contains the information about the offers. There are a total of 10 offers.
* **data/profile.json** - This was provided by Starbucks and contains demographic information about the customers. There are a total of 17,000 customer profiles.
* **data/transcript.json** - This was provided by Starbucks and contains information about a customer's purchases and their interaction with the offers. There are 306,534 events recorded
* **all_data_combine_clean.csv** - The final combined data after all preprocessing and analysis.
* **proposal.pdf**: This document contains the initial project proposal I submitted prior to necessarily beginning this project.
* **Starbucks_Capstone_notebook.ipynb** - My Jupyter Notebook containing all data exploration, cleaning, feature engineering, model building, hyperparameter tuning, and the results.
* **report.pdf** - My final report contains all my final results and analyses as performed in the accompanying Jupyter notebook.
* **README.md** - This file

# Python Libraries Used

* pandas
* matplotlib
* seaborn
* numpy
* re
* progressbar2
* scikit-plot
* sklearn




