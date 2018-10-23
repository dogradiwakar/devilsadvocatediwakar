---
layout: post
title: Installing Apache Spark on Ubuntu
description: >

author: author1
canonical_url:
categories: [Installations]
#tags:       [Life]
---
# Installing Apache Spark on Ubuntu

## Step 1: Install Java.

Check Java Version

java -version

![](/devilsadvocatediwakar/blob/gh-pages/_posts/2018/images/installing%20spark/1.png)

Else install java

First, update the package index by in your terminal typing:

sudo apt-get update

sudo apt-get install default-jdk

## Step 2: Install Scala

sudo apt-get install scala

![](/devilsadvocatediwakar/_posts/2018/images/installing%20spark/2.png)

Type scala into your terminal:
Scala
![](/devilsadvocatediwakar/_posts/2018/images/installing%20spark/3.png)

You should see the scala REPL running. Test it with:
println(“Hello World”)
You can then quit the Scala REPL with
:q



## Step 3: Install Spark
Next its time to install Spark. We need git for this, so in your terminal type:
sudo apt-get install git

![](/devilsadvocatediwakar/_posts/2018/images/installing%20spark/4.png)


Download latest Spark and untar it

sudo tar xvf spark-2.3.1-bin-hadoop2.7.tgz -C /usr/local/spark

![](/devilsadvocatediwakar/_posts/2018/images/installing%20spark/5.png)


Add Spark path to bash file

nano ~/.bashrc

Add below code snippet to the bash file

SPARK_HOME=/usr/local/spark
export PATH=$SPARK_HOME/bin:$PATH

Execute below command after editing the bashsrc
source ~/.bashrc
![](/devilsadvocatediwakar/_posts/2018/images/installing%20spark/6.png)

Go to the Bin Directory and execute the spark shell

./spark-shell

![](/devilsadvocatediwakar/_posts/2018/images/installing%20spark/7.png)



The web console is also available at below highlighted url

![](/devilsadvocatediwakar/_posts/2018/images/installing%20spark/8.png)


![](/devilsadvocatediwakar/_posts/2018/images/installing%20spark/9.png)

To Start both master and slave node execute below command

![](/devilsadvocatediwakar/_posts/2018/images/installing%20spark/10.png)


./Start-all.sh

The web ui will be available at 8080 port
![](/devilsadvocatediwakar/_posts/2018/images/installing%20spark/11.png)





[docs]: ../../docs/README.md
