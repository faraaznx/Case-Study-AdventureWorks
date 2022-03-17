<h3>Sqoop import command</h3>

sqoop import --connect jdbc:mysql://localhost:3306/adventureworks?useSSL=False --username root --password-file file:///home/saif/LFS/cohort_c9/envvar/sqoop.pwd --delete-target-dir --target-dir /user/saif/HFS/Input/adventureworks --query "select CustomerID,TerritoryID,AccountNumber,CustomerType,ModifiedDate,Demographics from customer_individual \
where \$CONDITIONS" --split-by CustomerID


<h3>Hive manage table & Load data in manage table</h3>
create table cust_indi(CustomerID int,TerritoryID int,AccountNumber string,CustomerType string,ModifiedDate timestamp,Demographics string) row format delimited fields terminated by ',' tblproperties("skip.header.line.count"="1") ;

load data inpath "/user/saif/HFS/Input/adventureworks/" into table cust_indi;

<h3>Load data in new table from manage table</h3>
create table ext_cust as select customerid,territoryid,accountnumber,customertype,modifieddate,xpath(demographics,'IndividualSurvey/TotalPurchaseYTD/text()'),xpath(demographics,'IndividualSurvey/DateFirstPurchase/text()'),xpath(demographics,'IndividualSurvey/BirthDate/text()'),xpath(demographics,'IndividualSurvey/MaritalStatus/text()'),xpath(demographics,'IndividualSurvey/YearlyIncome/text()'),xpath(demographics,'IndividualSurvey/Gender/text()'),xpath(demographics,'IndividualSurvey/TotalChildren/text()'),xpath(demographics,'IndividualSurvey/NumberChildrenAtHome/text()'),xpath(demographics,'IndividualSurvey/Education/text()'),xpath(demographics,'IndividualSurvey/Occupation/text()'),xpath(demographics,'IndividualSurvey/HomeOwnerFlag/text()'),xpath(demographics,'IndividualSurvey/NumberCarsOwned/text()'),xpath(demographics,'IndividualSurvey/CommuteDistance/text()') from cust_indi;


<h3>Sqoop import for credit card table</h3>
sqoop import --connect jdbc:mysql://localhost:3306/adventureworks?useSSL=False --username root --password-file file:///home/saif/LFS/cohort_c9/envvar/sqoop.pwd --delete-target-dir --target-dir /user/saif/HFS/Input/adventureworks1 --query "select CreditCardID,CardType,CardNumber,ExpMonth,ExpYear,ModifiedDate from creditcard \
where \$CONDITIONS" -m 1


<h3>Create manage table for credit card & Load data in manage table for credit card table</h3>
create table credit_hive(CreditCardID  int,CardType string,CardNumber bigint,ExpMonth int,ExpYear int,ModifiedDate timestamp ) row format delimited fields terminated by ','  tblproperties("skip.header.line.count"="1");
 
load data inpath "/user/saif/HFS/Input/adventureworks/" into table credit_hive;

<h3>Load data from hive to Pyspark & perform Transformation</h3>

<h3>Load data from Pyspark to hive and perform analytics</h3>
