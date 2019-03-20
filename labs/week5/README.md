# Week 5 Data Science Lab

## Introduction

This week's exercises can all be conducted on the Big Data cluster provided for the class.

You will be using the EPFL cluster for this exercise.

If you wish to experiment with advanced features that require admin privileges, we encourage you to try the Hortonworks HDP Sandbox from [Hortonworks](https://hortonworks.com/downloads/#sandbox). From there, you will have the option to download the Sandbox for VirtualBox or for Docker.

## Exercises series 1 - HDFS

### First steps
In this series of exercises you will experiment with the Hadoop Distributed File System (HDFS).

Open a terminal on your laptop and ssh to the cluster with your EPFL __gaspar__ username and password.

```shell
ssh your-gaspar-username@iccluster042.iccluster.epfl.ch
```

To get started with HDFS, type:

```shell
hdfs dfs
```

Notice how most of the commands behave like corresponding Unix commands.

### Exercises
As a first exercise, you will explore the content of the cluster's HDFS file system using the __hdfs dfs__ command.

1. We have created a directory on HDFS for each of you, can you find yours?
2. Create a folder __work1__ in your HDFS directory and change the access rights so that only you and group hadoop can read and write into it.
3.  Copy the 2017 _Traffic Count_ data published by the [Calderdale Metropolitan Borough Council (UK)](https://data.gov.uk/dataset/0c64970c-756a-46b2-9282-4a62016c7c64/traffic-count) to your __work1__ directory from. A copy of the data is also available from the [dslab 2019 github repository](https://github.com/dslab2019/dslab2019.github.io/blob/master/data/week5/01012017_to_31072017.csv.bz2?raw=true)

## Exercise series 2 - Hive

Hive is data warehouse built on top of Apache Hadoop. It is used to organize your data into tables on HDFS, and to executes SQL-like queries on them as Map Reduce jobs.

For this series of exercises we will use the Zeppelin notebook. This is yet anoter commonly used notebook, similar to Jupyter notebooks that you are already familiar with. We are using this notebook because it is installed by default with the Horthonworks HDP distribution.

Open a browser and log in the Zeppelin UI with your EPFL __gaspar__ username and password at [`https://iccluster042.iccluster.epfl.ch:9995/`](https://iccluster042.iccluster.epfl.ch:9995/) .

Once logged in, from your Zeppelin homepage, select the __import note__ option, and copy the URL of this class's [notebook](https://raw.githubusercontent.com/dslab2019/dslab2019.github.io/master/notebooks/DSLab_week5_Hive_Exercises.json) .

You can now open the notebook in Zeppelin and start working on the exercises. As a bonus you can repeat the same exercises using the __hive__ command in a terminal.

Data source in this exercise: [The twitter stream grab provided thanks to the internet archive](https://archive.org/download/archiveteam-twitter-stream-2018-10)
