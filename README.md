# Udacity-Starbucks-capstone-project

This work is due as final project of the data science program of Udacity.

Libraries used:

import pandas as pd
import numpy as np
import math
import json
from datetime import datetime
from time import time
import matplotlib.pyplot as plt
import seaborn as sns
import warnings
warnings.filterwarnings("ignore")
from sklearn.naive_bayes import GaussianNB
from sklearn.ensemble import AdaBoostClassifier
from sklearn.metrics import accuracy_score,f1_score
from sklearn.model_selection import train_test_split,GridSearchCV
from sklearn.naive_bayes import GaussianNB
from sklearn.neighbors import KNeighborsClassifier
from sklearn.svm import SVC
from sklearn.tree import DecisionTreeClassifier
from sklearn.preprocessing import MinMaxScaler

Project motivation:

Starbucks company has an online shop where they sell their products, mostly coffee drinks and related products. Through this online shop they have advertisements sent. Some of these advertisements are offers that they send everyday, in this case 2 offers, Bogo and Discount. Bogo offer consists of a buy one get one free and Discount offer consists of a discount on buying.
For this study the data used are 3 datasets, namely portfolio profile and transcript that come in a json format. These data are not real but they mimic real data, only one drink is advertised here.
3 questions were answered:
Which segment of population should be targerted with the advertisement?
Which advertisement succeded better?
Where does the advertisement a success?

Files description:

three files:

portfolio.json - containing offer ids and meta data about each offer (duration, type, etc.)
profile.json - demographic data for each customer
transcript.json - records for transactions, offers received, offers viewed, and offers completed

explanation of each file:

portfolio.json

id (string) - offer id
offer_type (string) - the type of offer ie BOGO, discount, informational
difficulty (int) - the minimum required to spend to complete an offer
reward (int) - the reward is given for completing an offer
duration (int) - time for the offer to be open, in days
channels (list of strings)
profile.json

age (int) - age of the customer
became_member_on (int) - the date when customer created an app account
gender (str) - gender of the customer (note some entries contain 'O' for other rather than M or F)
id (str) - customer id
income (float) - customer's income
transcript.json

event (str) - record description (ie transaction, offer received, offer viewed, etc.)
person (str) - customer id
time (int) - time in hours since the start of the test. The data begins at time t=0
value - (dict of strings) - either an offer id or transaction amount depending on the record

Results:

Answering the 3 questions, the best targeted bracket of respondants for the advertisement are people above 60 years, prefered Female and with income exceeding 60000 USD. The Discount advertisement succeded better than the Bogo advertisement and we try as models the K-Nearest neighbor, the AdaBoostClassifier and the DecisionTreeClassifier anf got a model that can predict if advertisements succeeded with a completion according to all the demographic and economics inputs of the provided datasets.

License I hereby put at the disposal of everyone the use of this program for free and thanks for Udacity for providing this simulation.
