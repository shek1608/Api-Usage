#Summary of Data Exploration

##Data Processing and Decision:

We started data exploration by picking stackoverflow data sets first. We used the stackoverflow database downloaded from [stackexchange database] (https://archive.org/details/stackexchange) to get the sample data sets (in XML format) in order to analyse the usage of different APIs. For this, the relevant tables in the stackoverflow database that would help in our goal are.

1. Posts (row Id, PostTypeId, AcceptedAnswerId, CreationDate, Score, ViewCount, Body, OwnerUserId, LastEditorUserId, LastEditDate, LastActivityDate, Title,Tags, AnswerCount, CommentCount, FavoriteCount)
2. Comments (row Id, PostId, Score, Text, CreationDate, UserId)

In the above, the *‘Body’* column of the **‘Posts’** and **‘Comments’** tables would be our main criterion to bifurcate and extract the data for different APIs. We run commands to search for particular keywords to identify usage of the APIs.

The keywords to be searched will be maintained in a structure. For this, we will be parsing through the javadocs and create a dictionary to maintain classes and methods.

The fields, *‘AcceptedAnswerId’* and *‘ClosedDate’* of the **‘Posts’** table can be used to analyse if the post has received an appropriate answer. This will give an idea as to what is the percentage of open and resolved questions for each API and where are some unanswered questions of some programmer’s which needs attention.


##Progress till now:

1. We have created a Hadoop cluster consisting of two nodes to facilitate the data management and extraction.
2. We have set up Apache Hive, where the database will be created, stored and queried using SQL.

##Road-ahead:

1. To port the xml data files into the hive tables and performing analysis to get results which will be later used for analyzing the goals of the project. 
2. Extracting results from the stored data sets.
3. Creating Visualizations for results.
