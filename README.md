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

Analytical Dashboard: PowerBI

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

![Screenshot 2024-09-22 at 12.21.48 PM.png](End-to-end%20Data%20Analytics%20Pipeline%20Project%201091e92f538e806e9c50e5d4e3775e72/Screenshot_2024-09-22_at_12.21.48_PM.png)

1. Create a table

![Screenshot 2024-09-22 at 12.19.42 PM.png](End-to-end%20Data%20Analytics%20Pipeline%20Project%201091e92f538e806e9c50e5d4e3775e72/Screenshot_2024-09-22_at_12.19.42_PM.png)

### Launch Jupyter Notebook:

<aside>
💡

I used **python version 3.10** for this

</aside>

For how to setup a Jupyter notebook using Anaconda read my blog: [My Anaconda + Jupyter Notebook Setup](https://www.notion.so/My-Anaconda-Jupyter-Notebook-Setup-1091e92f538e807ebe46e67414f223ae?pvs=21) 

Additionally you can read this if you are completely new to jupyter notebooks: https://www.dataquest.io/blog/jupyter-notebook-tutorial/

(If you want to use venv or something else that works too)

… Jupyter Notebook stuff

### Connect DB to Tableau and Make Dashboard

You will need Tableau Desktop:

Read this for instructions on connecting Postgres to Tableau: [https://help.tableau.com/current/pro/desktop/en-us/examples_postgresql.htm?_gl=1*1o9ogog*_ga*MTYxNzE2NjE5MC4xNzI3MDMxODQ2*_ga_8YLN0SNXVS*MTcyNzAzMTg0NC4xLjEuMTcyNzAzMjc0Mi4wLjAuMA](https://help.tableau.com/current/pro/desktop/en-us/examples_postgresql.htm?_gl=1*1o9ogog*_ga*MTYxNzE2NjE5MC4xNzI3MDMxODQ2*_ga_8YLN0SNXVS*MTcyNzAzMTg0NC4xLjEuMTcyNzAzMjc0Mi4wLjAuMA) 

Once you are in Tableau Desktop, you can 

![Screenshot 2024-09-22 at 2.18.42 PM.png](End-to-end%20Data%20Analytics%20Pipeline%20Project%201091e92f538e806e9c50e5d4e3775e72/Screenshot_2024-09-22_at_2.18.42_PM.png)

Enter in server information

![Screenshot 2024-09-22 at 2.44.29 PM.png](End-to-end%20Data%20Analytics%20Pipeline%20Project%201091e92f538e806e9c50e5d4e3775e72/Screenshot_2024-09-22_at_2.44.29_PM.png)

Finally, you can design sheets and dashboards. I have created a simple sheet with a Tree map, selecting Name, Symbol and Market Cap as Discrete Dimensions, while selecting Market cap as Continuous Measure for the detail and color.

![image.png](End-to-end%20Data%20Analytics%20Pipeline%20Project%201091e92f538e806e9c50e5d4e3775e72/image.png)

Finally, we can drag this Sheet into a new Dashboard to start making our own cryptoanalysis Dashboard

![image.png](End-to-end%20Data%20Analytics%20Pipeline%20Project%201091e92f538e806e9c50e5d4e3775e72/image%201.png)

## Conclusion:

You now have a working Tableau Dashboard that is connected to a PostgresSQL DB where data is loaded from an API. Python is used for ETL. 

### Additional Steps:

…