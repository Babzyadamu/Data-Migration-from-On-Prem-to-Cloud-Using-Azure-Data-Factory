# Data-Migration-from-On-Prem-to-Cloud-Using-Azure-Data-Factory

## Introduction
![](Intro_Pic.png)

This project was to migrate data from on Premise to the cloud using Microsoft Azure Data Factory.

Disclaimer!!!! The dataset utilized for this analysis was sourced from Kaggle,  Any findings, conclusions, or insights presented in this analysis are based on the data publicly available on Kaggle. 

## Problem Statement

Company xyz have their data on premises where they maintain and secure all their infrastructure however, In response to the escalating challenges of managing costly on-premises infrastructure, optimizing scalability, and ensuring robust data security, company xyz is ready to migrate to the cloud using Microsoft Azure.. This transition will help to unlock cost savings, enhance flexibility, and improve overall business agility while maintaining high standards of data protection and compliance. The final data is to be kept in a container on Microsoft Azure in a Csv format.


## Methodology
- Create a self-hosted gateway (integration run time) to connect to the on premise server that hosts the database.
-  Create two linked service in Azure Data Factory by choosing sql server as the link to the on premise data source as the first linked service and the second linked service by choosing Azure Data Lake Storage Gen 2 (Container where the Csv migrated data will be kept).
-  Create two new dataset to connect to the linked service created for the sql server as the first dataset and the second dataset to connect the Azure Data Lake Storage Gen 2 linked service which is a csv dataset.
-  Create a pipeline that will connect to the source data set (sql server on prem) and sink the data to the Azure Data Lake Storage Gen 2 storage where the data will be stored.
