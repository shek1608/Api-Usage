#Hive Queries on Data Set run on Hadoop:

First, start the terminal as root and cd into the Hadoop directory. Then run the following:

* Open Hive console
<br>***bin/hive start***

* Add the downloaded jar to the hive console
<br>***add jar localpath/hivexmlserde-x.x.x.x.jar;***

Now we are set up to run the Hive queries. The following are the queries with the API/class for which they are run:

* **Arrays:**

*select count(body) from posts lateral view explode(map_values(row_id)) x as body where body like “%Arrays%”;*

* **ArrayList:**

*select count(body) from posts lateral view explode(map_values(row_id)) x as body where body like “%ArrayList%”;*

* **LinkedList:**

*select count(body) from posts lateral view explode(map_values(row_id)) x as body where body like “%LinkedList%”;*

* **HashMap:**

*select count(body) from posts lateral view explode(map_values(row_id)) x as body where body like “%HashMap%”;*

* **HashSet:**

*select count(body) from posts lateral view explode(map_values(row_id)) x as body where body like “%HashSet%”;*

* **LinkedHashMap:**

*select count(body) from posts lateral view explode(map_values(row_id)) x as body where body like “%LinkedHashMap%”;*

* **TreeMap:**

*select count(body) from posts lateral view explode(map_values(row_id)) x as body where body like “%TreeMap%”;*

* **Vector:**

*select count(body) from posts lateral view explode(map_values(row_id)) x as body where body like “%Vector%”;*

* **File:**

*select count(body) from posts lateral view explode(map_values(row_id)) x as body where body like “%File%”;*

* **Jpanel:**

*select count(body) from posts lateral view explode(map_values(row_id)) x as body where body like “%JPanel%”;*

* **Jlabel:**

*select count(body) from posts lateral view explode(map_values(row_id)) x as body where body like “%JLabel%”;*

* **ActionEvent:**
*select count(body) from posts lateral view explode(map_values(row_id)) x as body where body like “%ActionEvent%”;*

* **MouseEvent:**

*select count(body) from posts lateral view explode(map_values(row_id)) x as body where body like “%MouseEvent%”;*

* **KeyEvent:**

*select count(body) from posts lateral view explode(map_values(row_id)) x as body where body like “%KeyEvent%”;*

* **IOException:**

*select count(body) from posts lateral view explode(map_values(row_id)) x as body where body like “%IOException%”;*

* **Java:**

*select count(body) from posts lateral view explode(map_values(row_id)) x as body where body like “%java%”;*

* **Swing:**

*select count(body) from posts lateral view explode(map_values(row_id)) x as body where body like “%JButton%” or body like “%JFrame%” or body like “%JTextField%” or body like “%JMenu%” or body like “%JPanel%” or body like “%JLabel%”;*

* **Synchronization:**

*select count(body) from posts lateral view explode(map_values(row_id)) x as body where body like “%Synchroniz%”;*

* **Server/ServerSocket:**

*select count(body) from posts lateral view explode(map_values(row_id)) x as body where body like “%Socket%” or body like “%ServerSocket%”;*

* **Thread/Runnable:**

*select count(body) from posts lateral view explode(map_values(row_id)) x as body where body like “%Thread%” or body like “%Runnable%”;*

* **Scanner:**

*select count(body) from posts lateral view explode(map_values(row_id)) x as body where body like “%Scanner%”;*

* **FileInputStream:**

*select count(body) from posts lateral view explode(map_values(row_id)) x as body where body like “%FileInputStream%”;*

* **BufferedReader:**

*select count(body) from posts lateral view explode(map_values(row_id)) x as body where body like “%BufferedReader%”;*

* **DataInputStream:**

*select count(body) from posts lateral view explode(map_values(row_id)) x as body where body like “%DataInputStream%”;*

* **FileOutputStream:**

*select count(body) from posts lateral view explode(map_values(row_id)) x as body where body like “%FileOutputStream%”;*

* **BufferedWriter:**

*select count(body) from posts lateral view explode(map_values(row_id)) x as body where body like “%BufferedWriter%”;*

* **DataOutputStream:**

*select count(body) from posts lateral view explode(map_values(row_id)) x as body where body like “%DataOutputStream%”;*

