# Implementation od CDC using Databricks & ADF with Email Notification

This is a Change Data Capture (CDC) project I implemented using **Azure Data Factory**, **SQL Server**, **Databricks**, and **Logic App**.  
The goal was to detect and reflect **INSERT**, **UPDATE**, and **DELETE** operations from a source table into a target system and **notify via email** automatically.

I designed it to run **every 3 min** for quick testing, but it can be scheduled hourly or as needed in production.

---

## Project Summary: 

• **Pipeline Name:** ls_samiksha-cdc_project  
• **Source:** Azure SQL Database (Change-tracked table)  
• **Sink:** Azure SQL or Data Lake  
• **Email Notifier:** Azure Logic App  

---

##  What It Does :

• Detects row-level changes (INSERT, UPDATE, DELETE) in a source table using CDC  
• Loads only changed data to the destination using **Databricks Notebook**  
• Sends an **email summary** after each run with number of inserted, updated, and deleted records

---

##  What I Used :

• Azure SQL Server with CDC enabled  
• Azure Data Factory V2  
• Azure Databricks  
• Azure Logic App (Email using Outlook connector)  
• GitHub for storing files and screenshots  

---

##  How It’s Scheduled :

• **Trigger Type:** Tumbling Window Trigger  
• **Trigger Frequency:** Every 3 minutes  
• **Pipeline Activities Used:**
  - Databricks Notebook
  - ForEach Activity
  - Web Activity (calls Logic App)

---
##  Sample Email Output: 
Subject: ADF Email Notification
Hi,
Here is the details of the updated CDC pipeline:
Table Name: Customer
Records Inserted: 5
Records Updated: 2
Records Deleted: 1
Thank you,
Samiksha Kharche

## What I Learned :

• How to set up and use Change Data Capture (CDC) on SQL Server  
• How to integrate Azure Data Factory with Databricks and Logic App  
• How to implement retry logic and parameter passing in ADF  
• How to trigger emails programmatically after pipeline completion  

---

## Author

**Samiksha Kharche**  
July 2025  

