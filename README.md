# End-to-end Data Analytics Pipeline Project

## Step 1: Stack Overview and Installations

### Project Overview:

**END to END Analytical Pipeline**

- Getting Data from an API
- Python + SQL for ETL (Extract, Transform, Load)
    - Extracted from API
    - Transformed using python (data cleaning)
    - Load - PostGressSQL
- Tableau - connected to the DB

Data Source: CoinCap

ETL Pipeline: Python, SQL

Data Warehouse: Postgres

Analytical Dashboard: Tableau

### Installations:

- Conda Installation (you can use venv or the default interpreter with a simple installation)
    - can use either miniconda or anaconda, does not matter
- PostGres Server
    - install and setup login
- PowerBI (can be done later)

## Step 2: Setup

### Setting up PostGres:

If you installed Postgres, run the pgadmin application

- it will likely take some time if it is your first
- you will be asked to create a password at some point, create something you will remember

1. Create a DB - name it something intuitive like 'CryptoStore’

![assets/Screenshot 2024-09-22 at 12.21.48 PM.png](https://github.com/B-a-1-a/CryptoDataAnalyticsPipeline/blob/main/assets/db1.png)

2. Create a table

![assets/Screenshot 2024-09-22 at 12.19.42 PM.png](https://github.com/B-a-1-a/CryptoDataAnalyticsPipeline/blob/main/assets/db2.png)

### Launch Jupyter Notebook:

<aside>
💡

I used **python version 3.10** for this

</aside>

For how to setup a Jupyter notebook using Anaconda read my blog: [My Anaconda + Jupyter Notebook Setup](https://www.notion.so/My-Anaconda-Jupyter-Notebook-Setup-1091e92f538e807ebe46e67414f223ae?pvs=21) 

Additionally you can read this if you are completely new to jupyter notebooks: https://www.dataquest.io/blog/jupyter-notebook-tutorial/

(If you want to use venv or something else that works too)

The source for the notebook is given, we basically "Extract" from API, Transform the data to remove Nas and load to postgres

After running refresh the DB and View all rows on the table:
![](https://github.com/B-a-1-a/CryptoDataAnalyticsPipeline/blob/main/assets/db3.png)

### Connect DB to Tableau and Make Dashboard

You will need Tableau Desktop:

Read this for instructions on connecting Postgres to Tableau: [https://help.tableau.com/current/pro/desktop/en-us/examples_postgresql.htm?_gl=1*1o9ogog*_ga*MTYxNzE2NjE5MC4xNzI3MDMxODQ2*_ga_8YLN0SNXVS*MTcyNzAzMTg0NC4xLjEuMTcyNzAzMjc0Mi4wLjAuMA](https://help.tableau.com/current/pro/desktop/en-us/examples_postgresql.htm?_gl=1*1o9ogog*_ga*MTYxNzE2NjE5MC4xNzI3MDMxODQ2*_ga_8YLN0SNXVS*MTcyNzAzMTg0NC4xLjEuMTcyNzAzMjc0Mi4wLjAuMA) 

Once you are in Tableau Desktop, you can 

![assets/Screenshot 2024-09-22 at 2.18.42 PM.png](https://github.com/B-a-1-a/CryptoDataAnalyticsPipeline/blob/main/assets/tab1.png)

Enter in server information

![assets/Screenshot 2024-09-22 at 2.44.29 PM.png](https://github.com/B-a-1-a/CryptoDataAnalyticsPipeline/blob/main/assets/tab2.png)

Finally, you can design sheets and dashboards. I have created a simple sheet with a Tree map, selecting Name, Symbol and Market Cap as Discrete Dimensions, while selecting Market cap as Continuous Measure for the detail and color.

![image.png](https://github.com/B-a-1-a/CryptoDataAnalyticsPipeline/blob/main/assets/tab3.png)

Finally, we can drag this Sheet into a new Dashboard to start making our own cryptoanalysis Dashboard

![image.png](https://github.com/B-a-1-a/CryptoDataAnalyticsPipeline/blob/main/assets/tab4.png)

## Conclusion:

You now have a working Tableau Dashboard that is connected to a PostgresSQL DB where data is loaded from an API. Python is used for ETL. 

### Additional Steps To Implement:

1. Deploy PostgreSQL on AWS RDS for scalability and automated backups.
2. Use AWS Lambda for serverless ETL and schedule it with CloudWatch Events.
3. Automate ETL with CloudWatch Events, Cloud Cron Jobs or Google Cloud/Azure Functions.
4. Host Tableau/PowerBI dashboards on AWS EC2/S3 or build custom ones with Plotly Dash.
5. Create a Flask/Django API to expose data and embed Tableau/PowerBI into web apps.
6. Implement CI/CD pipelines using GitHub Actions, Jenkins, or CircleCI for updates.
7. Dockerize the ETL pipeline, database, and dashboard for consistent deployment.
8. Monitor ETL jobs and database health using AWS CloudWatch and logging servic