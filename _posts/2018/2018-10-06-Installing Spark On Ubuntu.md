---
layout: post
title: Installing Apache Spark on Ubuntu
description: >

author: author1
canonical_url:
categories: [Installations]
#tags:       [Life]
---
Install Java


Check Java Version

java -version






Else install java


First, update the package index by in your terminal typing:

sudo apt-get update

sudo apt-get install default-jdk

Install Scala


sudo apt-get install scala






Type scala into your terminal:
Scala


You should see the scala REPL running. Test it with:
println(“Hello World”)
You can then quit the Scala REPL with
:q



Step 3: Install Spark
Next its time to install Spark. We need git for this, so in your terminal type:
sudo apt-get install git




Download latest Spark and untar it

sudo tar xvf spark-2.3.1-bin-hadoop2.7.tgz -C /usr/local/spark




Add Spark path to bash file

nano ~/.bashrc

Add below code snippet to the bash file

SPARK_HOME=/usr/local/spark
export PATH=$SPARK_HOME/bin:$PATH

Execute below command after editing the bashsrc
source ~/.bashrc


Go to the Bin Directory and execute the spark shell

./spark-shell





The web console is also available at below highlighted url






To Start both master and slave node execute below command




./Start-all.sh

The web ui will be available at 8080 port






[docs]: ../../docs/README.md
