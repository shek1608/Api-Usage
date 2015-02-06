#Steps to perform on our Hadoop Hive to read data into tables.

* Open Hive console
<br>***bin/hive start***

* Add the downloaded jar to the hive console
<br>***add jar localpath/hivexmlserde-x.x.x.x.jar;*** 

* Create table posts to handle the body, tags and other related content.

<br>***CREATE TABLE POSTS(row_id MAP<INT,STRING>)
ROW FORMAT SERDE 'com.ibm.spss.hive.serde2.xml.XmlSerDe'
WITH SERDEPROPERTIES (
"column.xpath.row_id" = "/row",
"xml.map.specification.row"="@Id->@Body")
STORED AS
INPUTFORMAT 'com.ibm.spss.hive.serde2.xml.XmlInputFormat'
OUTPUTFORMAT 'org.apache.hadoop.hive.ql.io.IgnoreKeyTextOutputFormat'
LOCATION "/apps/warehouse/"
TBLPROPERTIES (
"xmlinput.start"="<row ", 
"xmlinput.end"="/>");***<br>

* After creating the tables we can now load them with data. Follow these steps to load data into these tables. Run the below command just ONCE

<br>***load data local inpath '/opt/hadoop/post.xml' into table POSTS;***
