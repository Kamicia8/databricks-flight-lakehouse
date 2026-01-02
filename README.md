# databricks-flight-lakehouse

## Data Processing with Azure Databricks
Authors: Klaudia Stodółkiewicz & Kamila Ćwikła

---

Table of Contents:
* [Project Goal](#project-goal)
* [Data](#data)
* [Pipeline](#pipeline)
* [Environment Setup in Azure](#environment-setup-in-azure)
* [Prediction](#prediction)
* [Summary](#summary)
* [Links](#bibliography)

---

## Project Goal

The goal of this project is to build and showcase a data processing pipeline using Azure Databricks. The project showcases the entire data lifecycle-from ingestion from selected sources, through cleansing and preprocessing, to preparing the data for analytics and machine learning models.

## Pipeline


## Data

Analysis is based on the [2015 Flight Delays and Cancellations](https://www.kaggle.com/datasets/usdot/flight-delays) dataset. The data is stored in CSV format and comprises three relational tables: flights, airports, and airlines. With the primary table containing over 5.8 million records, the dataset is good for demonstrating distributed processing using Apache Spark. 

Additionally, the project incorporates the [NOAA JFK](https://www.kaggle.com/datasets/mexwell/noaa-weather-data-jfk-airport?select=jfk_weather.csv) dataset, which contains hourly weather observations from JFK Airport. The attributes include temperature, wind speed, humidity, visibility, and atmospheric pressure. By extracting data specifically for the year 2015, we can integrate it with the flight records from the same period. This allows for an in - depth analysis of how specific weather conditions impact flight delays at JFK Airport.

## Environment Setup in Azure

First, an [Azure account](https://portal.azure.com/?Microsoft_Azure_Education_correlationId=327084c6-9e36-466d-ba59-cf8557b1b7fd#view/Microsoft_Azure_Education/EducationMenuBlade/~/overview) was created. This project utilizes the Azure for Students subscription, which provides $85 in credits to explore and deploy cloud resources.

#### Environment Setup:

- `create resource` -> `Storage account` 

The `Storage Account`, named `newadbprojektkakastorage`, is responsible for the secure storage of data and its accessibility to other Azure services, such as Databricks, for further processing and analysis. During the setup, a new `Resource Group` named `rg_databrics_project` was created to serve as a logical container for all project-related resources.

<br>
<img src="images/s_account.png" width="700">
<br>
<img src="images/advn_s_account.png" width="700">

After completing these steps, the `Resources` tab in Azure appears as follows:

<br>
<img src="images/after_storage_gr_acc.png" width="700">

- `Storage account` -> `Data storage` -> `Container`

Creating a data container named `data`.

<br>
<img src="images/data_container.png" width="700">

- `Azure Databricks` -> `Create`

Creating a Databricks workspace named `new_databricks`.

<br>
<img src = "images/new_databricks.png" width="700">

It is important to ensure the following settings are applied in the `Networking` tab (avoiding a public IP helps to prevent unnecessary costs):

<br>
<img src = "images/what_was_causing_money.png" width="700">

Once created, click `Launch Workspace` to open the Databricks environment.

- `Databricks` -> `New` -> `Cluster` 

<br>
<img src = "images/create_cluster.png" width="700">

Next, we used the Kaggle API to download the datasets into the data container via the `load_data_from_kaggle.ipynb` notebook. The project workflow was also synchronized with GitHub using Databricks Repos for version control.

## Prediction

## Summary

## Links

- [Azure Databricks Documentation](https://learn.microsoft.com/en-us/azure/databricks/)
- [Databricks Repos - GitHub Integration](https://www.youtube.com/watch?v=Fnb4sA0hG8U)
- [How to make outputs visible on GitHub](https://learn.microsoft.com/en-us/azure/databricks/notebooks/notebook-format)




