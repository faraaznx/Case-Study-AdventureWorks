# Case-Study-AdventureWorks
<p><b>Business Problem</b>: HDFC Ltd is one of India's leading housing finance companies. HDFC Ltd offers a wide range of loan products such as Home Loans for new and resale properties and also offers credit cards. Credit cards are a convenient way of making any purchases from shopping to purchasing your favourite gadget to buying that new AC for your home to booking your flights & hotel and more or settling exorbitant bills when you don't have immediate funds at your disposal. HDFC from past 1 year is facing a issue related volume and variety of data so Its decide to transform data from RDBMS (MySQL) to HADOOP (hive).</p>

<h3>Technologies used to work in project</h3>
<ul>
<h4>Mysql</h4>
<h4>HDFS Ecosystem</h4>
  
<ul>
 <li>Sqoop</li>
 <li>Hive</li>
 <li>PySpark</li>
</li>
</ul> 
</ul>


<h3>Data Source Description</h3>
<p>&nbsp;&nbsp; &nbsp;&nbsp;  <b>Customer Test</b>: This table contain all customer data related information.</p>
<p>&nbsp;&nbsp; &nbsp;&nbsp;  <b>Individual Text</b>: This table contain all Individual data information.</p>
<p>&nbsp;&nbsp; &nbsp;&nbsp;  <b>Credit Card</b>: This table contain all credit card data information.</p>


![Untitled (12)](https://user-images.githubusercontent.com/100192276/158550587-0619c0ca-d35b-4db7-9e6c-e2d2789f6ab6.png)

# Steps performed to achive the task
<ul>
<li>Data is present in MySQL database.</li><br>
<li>Load the data from MySQL to HDFS using SQOOP.</li><br>
<li>Create and load data to HIVE table.</li><br>
<li>Read data from HIVE in Spark and perform data cleaning.</li><br>
<li>Load the data again to hive and perform analytics.</li><br>
</ul>

<h3>Project Architecture</h3>

![Untitled Diagram(1) (1)](https://user-images.githubusercontent.com/100192162/158647358-665077d2-c528-479c-83ec-4b345ae17109.jpg)
