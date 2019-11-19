![OVERVIEW](https://user-images.githubusercontent.com/19520346/69125846-7769b080-0af2-11ea-8de9-5cf021b2e0ba.PNG)

# Purpose
A cloud application solution for overtourism and promoting responsible travel by providing a platform where travellers explore destinations using a map displaying tourist-to-local ratios and view blogs filtered by their interests. It is a platform where responsible, conscientious travellers can be made. 

# Goals
1.	educate travellers
2.	show only relevant posts
3.	informative map
4.	improve quality of travel blogs

# Technologies
![tech](https://user-images.githubusercontent.com/19520346/69107831-6dc65580-0abe-11ea-9e97-77a83787938f.png)

The application was written in Django and React, deployed on Google App Engine through docker and Firebase respectively, the database hosted on Cloud SQL and the file storage on Cloud Storage. BigQuery was used to query data from the World Bank dataset, Apache Spark clusters were managed via Dataproc in which a Scala program was run using SparkSQL, as well as an Apache Zeppelin notebook for data analysis using Scala and a Jupyter notebook to create a linear regression model with PySpark. 

# Workflow
![workflow](https://user-images.githubusercontent.com/19520346/69107833-6ef78280-0abe-11ea-97e9-7345c40b4363.png)

There are three parts to this project:

### 1. Develop
- Backend: See [shared-world-backend](https://teanlouise.github.io/shared-world-backend)
- Frontend: See [shared-world-frontend](https://teanlouise.github.io/shared-world-frontend) 

### 2. Deploy: 
See more details [here](/deploy.md)

### 3. Data: 
See [shared-world-data](https://teanlouise.github.io/shared-world-data)
