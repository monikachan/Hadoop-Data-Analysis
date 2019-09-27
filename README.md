# Hadoop-Data-Analysis
<b>Cloud Computing Homework4</b><br>

The data was collected from the City of New York’s data website, and contains all reports of vehicular incidents in New York City over a period of time.We have developed the mapper and reducer scripts  that analyze the data and yield summary counts for each vehicle involved in an accident

<b>Environment used for Program Execution</b><br>
The Hadoop Cluster of University of Cincinnati was used to execute the Mapper and Reducer program coded in java<br>

<b>Steps to execute the program in Hadoop</b><br>
1.Copy the file cloud.java into the home directory<br>
2.Compile the program using the below command<br>
$hadoop com.sun.tools.javac.Main cloud.java <br>
3.Create jar file<br>
$ jar cf wc.jar cloud*.class<br>
4.Application Execution<br>
$ hadoop jar wc.jar cloud /user/tatavag/nyc.data /user/chandrmk/output<br>

<b>Mapper Functionality </b><br>
It picks the values of vehicle type and generate a key,value pair as follows <Vehicle_Type,count><br>
Example:<Truck,1><br>

<b>Reducer Functionality</b><br>
It gets the key,value pairs and adds up the count for all the key that has same value<br>
Example:<Truck,5><br>



