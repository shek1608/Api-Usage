#Hadoop Configuration Steps:

At first, we need to create a keyless ssh-keygen for both machines to enable ssh without passwords.

On both the nodes, do the following:

1. setenforce 0 (to disable SE Linux)

2. Permanently disabling SELinux so that on system reboot it does not restart is strongly recommended. To do this, edit the SELinux config and set SELINUX to disabled. On each host:
*vi /etc/selinux/config*
*SELINUX=disabled*

3. Disable iptables
*/etc/init.d/iptables stop*


4. open /etc/yum/pluginconf.d/refresh-packagekit.conf
Set *enabled=0*

5. Write *umask 022*

6. create hadoop folder in root and untar the .gz file

7. create java folder in root and untar the .gz file

8. .bashrc:
*export JAVA_HOME=$HOME/java/jdk1.7.0_71*
*export PATH=$JAVA_HOME/bin:$PATH*

9. Do *vi conf/hadoop-env.sh:*
Add:
*export JAVA_HOME=$HOME/java/jdk1.7.0_71*

10. Next gedit conf/core-site.xml:

```xml
<property>

 <name>hadoop.tmp.dir</name>

 <value>/root/hadoop/tmp</value>

 <description>A base for other temporary

 directories.</description>

</property>

<property>

 <name>fs.default.name</name>

 <value>hdfs://192.168.184.188:54310</value>

 <description>The name of the default file system. A URI whose scheme and authority determine the FileSystem implementation. The uri's scheme determines the config property fs.SCHEME.impl)  naming the FileSystem implementation class. The uri's authority is used to determine the host, port, etc. for a filesystem.
 </description>

</property>

//put masters ip and /root ie locaton of hadoop
```

11. vi mapred-site.xml:

```xml
<property>

 <name>mapred.job.tracker</name>

 <value>192.168.184.188:54311</value>

 <description>The host and port that the MapReduce job tracker runs at. If "local", then jobs are run in-process as a single map and reduce task.

 </description>

</property>
//put masters ip
```

12. vi hdfs-site.xml:

```xml
<property>

 <name>dfs.replication</name>

 <value>2</value>

 <description>Default block replication.

 The actual number of replications can be specified when the file is created. The default is used if replication is not specified in create time.

 </description>

</property>

//Have put 2 since we have a 2 node cluster
```

13. From Hadoop folder in Master, run:
bin/start-all.sh

14. Run jps on both machines to check.


