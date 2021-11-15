# Pyspark_int_qust
Company Name ***************

Round 1 :

1. What is closure in python?

2. How to declare static variable in python ?

3. Write a program to sum the below inputs.

case 1 : i/p : "1234"
case 2 : i/p : "12345abcd"

4. Write a program to reverse each of the word in a given string.

i/p : Hi I am Henry and i am a data Scientist . Hello Saurav ! You are a data Engineer.


5. Write a program to check the number is prime or not.


6. How to set the insertion ordered for a dictionary python object.


7. What will happen when will create the object for parent class and invoke it.

8. Major difference b/w list and tuple.


9. Spakr key componments interms of data processing.

10. What is the role of map partition ?

11. What is the key difference b/w persist and broadcast ?

12. Suppose five jobs are running in a parallel for spark application and suddenly 3 jobs failed how to see those failed job for further analysis.

Please note don't use YARN Log application id .Please think different solution here.

Answer : SparkHistory Server.

13. Difference b/w fold and zip ?

14. We are running one pyspark application in a cluster and job is taking more than one and haLF HOURs time to complete .

What are the prerequiste techniques can be used in spark to run the job in faster way.

15. Sqoop how to set bounary query condition.

16. Write a sql query to find the 7th highest salary for each departments.

17. Can we use where clause after group by ?

18. Suppose i have a file in hdfs layer and that file is kind of semi-structured data (ip_address file for one counrty).

How to create a dataframe for such types of files with correct schema .

19.What is the command to remove the files permannently from the Trash.

Answer : set purge=true and skiptrash command have to used to remove the files permannently.


Round 2:

1. What are Generators in python.

2. Difference b/w python functions and Generators.

3. Can we make set as a ordered set .

4. In your project have you used the encapsulation concept .

5. What is list compression and how it is different than lambda in python.

6. What command do we have to validate the columns in sqoop while importing the data from Oracle/Mysql.

7. Why reducer not comes into the picture while importing the data from sqoop.

8. Command for import the data direct to the hive table.

9. Difference b/w hive internal and external table.

10. Difference between map side join and smb join in hive.

11. How to fix the small files issues for spark and hive.

12. What are the key differences between transformation and action?

13. Explain the lineage graph.

14. WHAT IS the role of the dag scheduler.

15. Suppose we have a large table and small table which join will suit better here.

16. Suppose i have a one small table whose size is 1.5 gb and 9 executors we have in a cluster .How much memory will be consumed by the small table in the executors.

17. Spark submit parameters explain.


**************************************************2nd Company Questions *********************************************
1st round Data Engineer Questions :

1. Explain the spark architecture .

2. Difference between persist and broadcast.

3. Use cases of fold and accumulator.

4. Difference between RDD and Dataframe.

5. "TOO LARGE DATAFRAME " production issue how to handle.

6. Small file issues in HDFS how to resolve it ?

7. Hive map side join use cases.

8. SMB join and bucket join difference.

9. Hive optimization techniques.

10. Write a program to find the 3rd highest number in a below list (Python).

L1=[10,23,45,67,89,34,45,10,67]


11. How to create a dict with below two given lists.

Names=['Suman','Rakesh','Neha']

Salary=[20000,35000,45000]

o/p ={'Suman':20000} like this

12. What is frozen set in Python

13. Write a program to reverse the each string .

i/p

s1="Hi Saurav ,Hope you like the Wipro Organization "


2nd Round Interview :

1. What is Sarrogate key in Spark.

2. Spark optimization techniques used in your projeect please explain.

3. Repartion vs Coalese difference.

4. Write a sql query to fetch the 7th highest salary from each of the department.

Scenario based question.

Want to replace where ever JIO with "JIO INDIA limited"

write a program in dataframe to handle this scenario.

**************************************************3rd Company *********************************************

Company Name : XYZ 

1. How to connect orcale in pyspark

2. Repartion and coalesce difference
3. Hive optimization techniques
4. We have 7mb of file in hive want to join with some other big table which join will be best approch ?

Ans : Map side join

5. Sqoop incremental command for fetch the output from rdms.

6. Splitby why used and y reducer not triggering in sqoop which fetching the records.

7. There is a array i want 2nd highest data from the array.

input=(10,23,43,-2,78,34)
o/p: 43

Please write a code without sort function.

6. There is a below data frame and i want 2nd highest sal for the different name.

i/p dataset:

 id,name,sal,date
101,ABC,100,2020-01-01
102,xyz,600,2020-02-01
103,pqr,900,2020-03-01
104,ABC,300,2020-01-01
105,ABC,400,2020-01-01
106,xyz,700,2020-02-01
107,pqr,400,2020-03-01


output:
102,xyz,600,2020-02-01
104,ABC,300,2020-01-01
107,pqr,400,2020-03-01

pyspark.sql.window import Window
from pyspark.sql.functions import row_number
windowSpec  = Window.partitionBy("name").orderBy(sal).desc()
df.withColumn("row_number",row_number().over(windowSpec).where("row_number"==2))
    .show(truncate=False)


code written above.

7. How to add the cast for decimal columns to Integer datatype.

8. how to addthree union tablesin dataframe.

i/p df1 ,df2 and df3.

sol: df4=df1.union(df2).union(df3)

9. Want no duplicate for any of the rows for above dataframes.

sol : df4=df1.union(df2).union(df3).distinct()

10 .Below dataframe  see the o/p and give the solution.

id,name,sal,date
101,100,2020-01-01
102,600,2020-01-01
101,300,2020-01-01
101,400,2020-01-01
102,700,2020-01-01

 output
101,[100,300,400],2020-01-01
102,[600,700],2020-01-01

anser: pivotDF = df.groupBy("id").array(pivot("sal"))

pivotDF.show(truncate=False)


11. How to remove the duplicates from a list without using set.

i/p =[2,3,4,5,2,5]

o/p: [2,3,4,5]

12. Difference between repartion and partionby

13. Brodcast join explain

14. Below give i/p.

i/p : D1
 000123
 000456
 0001234
 0000012345000
 O/P :
 123
 456
 1234
 12345
 
 Use the regex_expr with withcolumn() transaforamtion to solve this question.
 
 15. What are the parameters you passed in spark -submit job in production.
 
 16. How to replace null value of city column with unkonwn in the below dataframe.
 
 i/p : City
   DEL
   MUM
   BLR
   NULL
   CHN
   PUNE
   
   O/P :
   CITY
   DEL
   MUM
   BLR
   Unknown
   CHN
   PUNE
   
   
   **************************************4th Company ****************************************
   Company Name xyz First Round Interview 

1. Why spark used for processing engine spark is only meant for processing?

2. Different file formats parquet and orc difference.

3. How to check the size of dataframe?

4. What is the difference between cache and persist ?

5. What will be ideal scenario when have to persist or cache the dataframe or rdd ?

6. Explain the partionby and bucketby in spark and when to use in production.

7. What types of modes in dataframeWriter Api.

8. Explain the spark context and spark session and its uses as well?

9. Difference b/w join and union explain with a query as well?

10. What is DAG and how its different from lineage graph.

11. Suppose our one spark job failed how to check and what will be the steps to recover the job.

12. What is the role of catalyst optimizer in spark dataframe.

13. Broadcast join and Shuffle join when to use.

14. Dataframe how to add a column from existing column data)

Ans : df.withcolumn("NewColumn",expr(placed the orginal column from which want to derived value
))

15. Explain the stage and task in spark.

16. difference between yarn client and yarn cluster and when to use.

17. Write a example for how to create rdd with different types.

18. Write a program to eliminate the duplicate from a list.

L1=(1,3,4,6,13,67,2,3,1)

19. In hive suppose we have a serde table and one is without serde table will able to see the data from both the table or not ?If not what will be the reason.

20. Hive partion and bucket explain with a example.How bucket store the data .

21. How to see the correct the records for semi-structured(xml) data in hive.

22. Difference between hive and Spark.

23. Spark can run without hadoop ?

24. Repartition and partionby difference.In production which one is used most.

25. What are the joins supported by spark dataframe

26. Role of accumulator in spark.

2nd Round(10 mins )

1. We have a two files f1 and f2 with below data.

f1= a b c
f2= c d e

Want the value c through code.

2. We have a file in hdfs with 10 records for id int column however for 9th and 10th position we have string value.

What will happen when load this file in hive table ?


3. Difference between rdd and dataframe .

Don't tell me the theory part tell me the programatically approach and which is the best

4. Have you ever worked in spark for window functioning.

Yes i used DenseRank(),Row_Number().
