# Case-Study-AdventureWorks
<h3><b>Aim</b></h3> 
 To perform Hive analytics on Sales and Customer Demographics data using big data tools such as Sqoop, Spark, and HDFS..</p>
 
<h3><b>Problem Statement</b></h3> 
We will dig deeper into some of the Hive's analytical features for this hive project. Using SQL is still highly popular, and it will be for the foreseeable future. Most big data technologies have been modified to allow users to interact with them using SQL. This is due to the years of experience and expertise put into training, acceptance, tooling, standard development, and re-engineering. So, in many circumstances, employing these excellent SQL tools to access data may answer many analytical queries without resorting to machine learning, business intelligence, or data mining.

This big data project will look at Hive's capabilities to run analytical queries on massive datasets. We will use the Adventure works dataset in a MySQL dataset for this project, and we'll need to ingest and modify the data. We'll use Adventure works sales and Customer demographics data to perform analysis and answer the following questions:
<li>Which age group of customers contribute to more sales?</li><br>
<li>To find the upper and lower discount limits offered for any product</li><br>
<li>To find the upper and lower discount limits offered for any product</li><br>
<li> Sales contributions by customer</li><br>
<li>To Understand customer persona purchasing pattern based on gender, education and yearly incomer</li><br>
<li>To find the sales contribution by customers on the overall year to date sales belong to categorized by same gender, yearly income.</li><br>
<li>To identify the top performing territory based on sales</li><br>
<li>To find the territory-wise sales and their adherence to the defined sales quota.</li><br>

<h3>Technologies used to work in project</h3>
<ul>
<h4><li>Mysql</li></h4>
<h4><li>HDFS Ecosystem</li></h4>
  
<ul>
 <li>Sqoop</li>
 <li>Hive</li>
 <li>PySpark</li>
</li>
</ul> 
</ul>


<h3>Data Source Description</h3>
<p> Adventure Works is a free sample database of retail sales data. In this project, we will be only using Customer test, Individual test, Credit card, Sales order details, Store, Sales territory, Salesperson, Sales order header, Special offer tables from this database. </p>

<p>&nbsp;&nbsp; &nbsp;&nbsp;  <b>Customer Test</b>: This table contain all customer data related information.</p>
<p>&nbsp;&nbsp; &nbsp;&nbsp;  <b>Individual Text</b>: This table contain all Individual data information.</p>
<p>&nbsp;&nbsp; &nbsp;&nbsp;  <b>Credit Card</b>: This table contain all credit card data information.</p>


![Untitled (12)](https://user-images.githubusercontent.com/100192276/158550587-0619c0ca-d35b-4db7-9e6c-e2d2789f6ab6.png)

# Project Architecture

![Untitled Diagram(1) (1)](https://user-images.githubusercontent.com/100192162/158647358-665077d2-c528-479c-83ec-4b345ae17109.jpg)

# Steps performed to achive the task
<ul>
<li>Create tables in MySQL database.</li><br>
<li>Load data from MySQL into HDFS storage using Sqoop commands.</li><br>
<li>Move data from HDFS to Hive.</li><br>
<li>Integrate Hive into Spark and perform data cleaning.</li><br>
<li>Using Pyspark, extract Customer demographics information from data and store it as parquet files.</li><br>
<li>Move parquet files from Spark to Hive.</li><br>
<li>Create tables in Hive and load data from Parquet files into tables.</li><br>
 <li> Perform Hive analytics on Sales and Customer demographics data.</li><br>
</ul>
