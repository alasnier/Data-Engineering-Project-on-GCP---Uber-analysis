# Data Engineering Project on GCP :cloud: -> Uber analysis :taxi:

<br>

# Introduction
Data engineering is a crucial aspect of any data-driven organization. It involves the collection, transformation, and storage of data to enable efficient data analysis and decision-making processes.

This project provides a framework and set of tools to facilitate various data engineering tasks, such as data ingestion, data integration, data processing and reporting dashboard.

<br>

# Roadmap 🗺
From raw data to report

1. Extract datas from "NYC Taxi & Limousine Commission"
2. EDA (Exploratory Data Analysis) with Jupyter Notebooks
3. Store raw datas on a datalake: GCP Cloud storage
4. ETL Process with Mage-AI and GCP Compute engine
5. Push golden datas into a data warehouse GCP BigQuery
6. Create a web dashboard with Looker Studio by Google

<br>


# Architecture 🏭
<img src="img\final_project_architecture.jpg">

<br>


# Programming language :black_nib:
Python and SQL

<br>
<br>
<br>
<br>
<br>

# My notes :pencil2:

:cloud: GCP Cloud Storage = AWS S3 = Azure Blob Storage
⇒ Store data → DataLake
<br>

:cloud: GCP Compute Engine = AWS EC2 = Azure xxxx
⇒ Virtual Machine
<br>

:cloud: GCP BigQuery 
⇒ SQL Queries → DataWareHouse
<br>

:cloud: GCP Looker Studio
⇒ Data Viz → Dashboard

<br>

🧙 Mage AI
⇒ OpenSource data pipeline

<br>

📇 <ins>Fact vs Dimension tables</ins><br>
quantitative datas, that change frequently and used for analysis<br>
vs.<br>
describe datas and attributes for grouping or filtering. They don’t change frequently

<br>

## Datas

1. Obtain datas
2. Learn, understand and gold the datas (clean, data dictionary, draw a data model and code it)
→ Lucid Charts or [draw.io](http://draw.io) by Google for the data model
→ Visual Studio Code or Jupyter Notebook for explore datas and apply data model

<br>

## Cloud

1. Create GCP Project
2. Create GCP Bucket and upload datas into it
Don’t forget to put your bucket and datas in “Public” mode
3. Create GCP Compute Engine Instance
4. Open SSH of the instance to launch Mage AI and/or install libraries on instance

1. Write `mage start project-name` to launch the project on mage 
2. Give the access from your GCP Compute Engine Instance by adding rule into firewall 
”Interfaces réseau” → open in new tab by the “name”  → on the left panel, choose firewall → add a new rule → add 0.0.0.0/0 in IP adresses and the local port in TCP
3. Open a enter external IP adress of the ComputeEngine Instance + ‘:’ + local port
⇒ 34.163.208.239:6789 for example

<br>

## Mage AI

1. Upload datat with API “Data loader” block
Obtain the API URL into GCP CloudStorage → Bucket → on the line of data wanted.
2. Transform / Goldify your datas by applying data model coded into a notebook previously 
3. Push your Golden datas into GCP BigQuery
!Don’t create the dataset on BigQuery, it’ll do it for you when you specify the name

<br>

## Cloud_2

1. Write you SQL Queries wanted to analyse
2. Create + complete your dashboard with LookerStudio

<br>
<br>
<br>
<br>
<br>

#
Enjoy exploring the world of data engineering with this project! If you have any questions, feedback, or issues, please don't hesitate to open an issue on the repository. Happy coding!
