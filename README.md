# Snowflake Azure Project to build real-time Twitter feed dashboard

In this Snowflake Azure project, you will ingest generated Twitter feeds to Snowflake in near real-time to power an in-built dashboard utility for obtaining popularity feeds reports.  

๐๐๐๐ถ๐ป๐ฒ๐๐ ๐ข๐๐ฒ๐ฟ๐๐ถ๐ฒ๐:  
Companies miss opportunities and are exposed to risk as a result of delays in company operations and decision-making. Organizations can move rapidly based on real-time data since it reveals issues and opportunities. Data that is gathered, processed, and evaluated in real-time is referred to as real-time data, and it comprises data that is ready to utilize as soon as it is created. A snapshot of historical data is what near real-time data is. When speed is critical, near real-time processing is preferred, although processing time in minutes rather than seconds is acceptable. Batch data that has been previously stored is considerably slower, and by the time it is ready to use, it might be days old.  

In this project, we ingest generated Twitter feeds to Snowflake in near real-time that will power an in-built dashboard utility in Snowflake to obtain popularity feeds reports.  

๐๐ฎ๐๐ฎ ๐ฃ๐ถ๐ฝ๐ฒ๐น๐ถ๐ป๐ฒ:  
A data pipeline is a technique for transferring data from one system to another. The data may or may not be updated, and it may be handled in real-time (or streaming) rather than in batches. The data pipeline encompasses everything from harvesting or acquiring data using various methods to storing raw data, cleaning, validating, and transforming data into a query-worthy format, displaying KPIs, and managing the above process.  

๐๐ฎ๐๐ฎ๐๐ฒ๐ ๐๐ฒ๐๐ฐ๐ฟ๐ถ๐ฝ๐๐ถ๐ผ๐ป:  
We will use the Twitter API and fetch tweets and their metadata(re-tweets, comments, likes) using Python.  

๐ง๐ฒ๐ฐ๐ต ๐ฆ๐๐ฎ๐ฐ๐ธ:  
โLanguage: Python  
โServices: Azure Storage Account, Azure Queue, Snowpipe, Snowflake, Azure Resource Group  

๐ฆ๐ป๐ผ๐๐ณ๐น๐ฎ๐ธ๐ฒ:  
Snowflake is a data storage, processing, and analytics platform that blends a unique SQL query engine with a cloud-native architecture. Snowflake delivers all the features of an enterprise analytic database to the user. Snowflake components include:  
Warehouse/Virtual Warehouse  
Database and Schema  
Table  
View  
Stored procedure  
Snowpipe  
Stream  
Task  

๐๐๐๐ฟ๐ฒ ๐ค๐๐ฒ๐๐ฒ:  
Azure Queue Storage allows application components to communicate in the cloud. Application components are frequently separated when developing for scale so that they may scale independently. Queue Storage enables asynchronous communications between application components operating in the cloud, on the desktop, on an on-premises server, or a mobile device. Queue Storage also allows you to manage asynchronous activities and create process workflows.  

๐๐ฝ๐ฝ๐ฟ๐ผ๐ฎ๐ฐ๐ต:  
โWe write API calls to fetch Twitter insights in real-time via Python and this code can be run in a local machine every day once.  

โWe create a Snowpipe component in Snowflakes using Azure IAM integration(cross-account access) as Snowflakes hosted on the Azure account is different from the Azure account we own. This in turn uses Azure EventGrid and Function App in the backend to automate the file load.  

โAs soon as the script generates files in Azure Blob storage, Snowpipe recognizes the file arrival and loads the snowflakes table with file data automatically.  

โWe create a dashboard in Snowflakes that is scheduled to refresh every 30 mins to show actual feed data from Twitter, Eg. No of likes and comments/feed to understand popular feed and their sentiment.  

![image](https://user-images.githubusercontent.com/70576003/196201351-42b3568b-69da-4dd6-b18a-e21a49af5051.png)  

๐๐ฒ๐ ๐ง๐ฎ๐ธ๐ฒ๐ฎ๐๐ฎ๐๐:  
โ Understanding the project overview.    
โ Creating Snowflake Account.  
โ Setup Twitter developer account.  
โ Deep Dive into Azure Storage Account.  
โ Understanding different components of Azure Storage Account.  
โ Azure Storage Account creation.  
โ Creating Storage Queue.  
โ Integrating Azure Queue and Snowflake.  
โ Creating Snowpipe Objects.  
โ Creating Snowflake Dashboard.  

Installation steps here..
https://github.com/Ajay026/Snowflake-Azure-Project/tree/main/Installation%20and%20Execution

Source code here..
https://github.com/Ajay026/Snowflake-Azure-Project/tree/main/Code

