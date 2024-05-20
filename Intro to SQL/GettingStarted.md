#Intro
- SQL - programming language used with the databases.
- Big Query, a web service that lets you apply SQL to huge datasets.

#importing big query from google cloud module
<from google.cloud import bigquery>

#create a client object
<client = bigquery.Client()>

#In big query each dataset is contained in a corresponding project

#constructing a reference to the "hacker_news" dataset
<dataset_ref = client.dataset("hacker_news", project="bigquery-public-data")>
# here the hacker_news dataset is part of the bigquery-public-data project

#To fetch the dataset - API request
<dataset = client.get_datset(dataset_ref)>