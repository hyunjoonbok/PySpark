# PySpark

![logo](./img/spark.png)

Spark is a great language for performing exploratory data analysis at scale, building machine learning pipelines, and creating ETLs for a data platform. Spark is a must for anyone who is dealing with Big-Data. Using PySpark (which is a Python API for Spark) to process large amounts of data in a distributed fashion is a great way to manage large-scale data-heavy tasks and gain business insights while not sacrificing on developer efficiency. In a few words, PySpark is a fast and powerful framework to perform massive distributed processing over resilient sets of data.

<hr>

## Motivation

I felt that any organization that deals with big data and data warehouse, some kind of distributed system needed. Being one of the most widely used distributed system, Spark is capable of handling several petabytes of data at a time, distributed across a cluster of thousands of cooperating physical or virtual servers. But most importantly, it's simple and fast. 

I thought data professionals can benefit by learning its logigstics and actual usage. Spark also offers Python API for easy data managing with Python (Jupyter). So, I have created this repository to show several examples of PySpark functions and utilities that can be used to build complete ETL process of your data modeling. The posts are more towards people who are already familari with Python and a bit of data analytics knowledge (where I often skip the enviornment set-up). But you can always follow the [Installtation section](Installation) if not familiar, then you should be able follow the notebook with no big issues. PySpark allows us to use Data Scientists' favoriate [Jupyter Notebook](https://jupyter.org/) with many pre-built functions to help processing your data. The contents in this repo is an attempt to help you get up and running on PySpark in no time!

<hr>

## Table of contents
* [Installation](#Installation)
* [PySpark Notebooks](#PySpark)
* [Contact](#Contact)
* [Reference](#Reference)

<hr>

## Installation

Downloading PySpark on your local machine could be a little bit tricky at first, but 

First things First, make sure you have Jupyter notebook installed

1. Install Jupyter notebook

```
pip install jupyter notebook
```

2. Install PySpark
Make sure you have Java 8 or higher installed on your computer. 
But most likely Java 10 would through an error. The recommended solution was to install Java 8 (Spark 2.2.1 was having problems with Java 9 and beyond)

Of course, you will also need Python (I recommend > Python 3.5 from Anaconda).
Now visit the [Spark downloads page](http://spark.apache.org/downloads.html). Select the latest Spark release, a prebuilt package for Hadoop, and download it directly.


3. Set the environment variables:

```
SPARK_HOME = D:\Spark\spark-2.3.0-bin-hadoop2.7
PATH += D:\Spark\spark-2.3.0-bin-hadoop2.7\bin
```

4. For Windows users,
- Download winutils.exe from here: https://github.com/steveloughran/winutils
- Choose the same version as the package type you choose for the Spark .tgz file you chose in section 2 “Spark: Download and Install” (in my case: hadoop-2.7.1)
- You need to navigate inside the hadoop-X.X.X folder, and inside the bin folder you will find winutils.exe
- If you chose the same version as me (hadoop-2.7.1) here is the direct link: https://github.com/steveloughran/winutils/blob/master/hadoop-2.7.1/bin/winutils.exe
- Move the winutils.exe file to the bin folder inside SPARK_HOME (i.e. C:\Spark\spark-2.3.0-bin-hadoop2.7\bin)
- Set the folowing environment variable to be the same as SPARK_HOME:
HADOOP_HOME = D:\Spark\spark-2.3.0-bin-hadoop2.7


5. Restart (our just source) and Run pyspark command your terminal and launch PySpark:
```
$ pyspark
```

For video instruction of installtion on Windows/Mac/Ubuntu Machine, please refer to each of the YouTube links below
- Windows [Link](https://medium.com/@GalarnykMichael/install-spark-on-windows-pyspark-4498a5d8d66c)
- Mac [Link](https://medium.com/@GalarnykMichael/install-spark-on-mac-pyspark-453f395f240b)
- Ubuntu [Link](https://medium.com/@GalarnykMichael/install-spark-on-ubuntu-pyspark-231c45677de0)

Or More Blogs I found on installations steps
- https://towardsdatascience.com/how-to-get-started-with-pyspark-1adc142456ec
- https://medium.com/big-data-engineering/how-to-install-apache-spark-2-x-in-your-pc-e2047246ffc3


<hr>

## PySpark

These examples display unique functionalities available in PySpark. They cover a broad range of topics with different method that user can utilize inside PySpark.


   #### [PySpark and SparkSQL Complete Guide](https://github.com/hyunjoonbok/PySpark/blob/master/PySpark%20and%20SparkSQL%20Complete%20Guide.ipynb) 
   <p>
    Apache Spark is a cluster computing system that offers comprehensive libraries and APIs for developers, and SparkSQL can be represented as the module in Apache Spark for processing unstructured data with the help of DataFrame API. In this notebook, we will cover the basics how to run Spark Jobs with PySpark (Python API) and execute useful functions insdie. If followed, you should be able to grasp a basic understadning of PySparks and its common functions. 
	</p>
  
   #### [PySpark Dataframe Complete Guide (with COVID-19 Dataset)](https://github.com/hyunjoonbok/PySpark/blob/master/PySpark%20Dataframe%20Complete%20Guide%20(with%20COVID-19%20Dataset).ipynb) 
   <p>
    Spark which is one of the most used tools when it comes to working with Big Data, but whereas Spark used to be heavily reliant on RDD manipulations, Spark has now provided a DataFrame API for us Data Scientists to work with. So in this notebook, We will learn standard Spark functionalities needed to work with DataFrames, and finally some tips to handle the inevitable errors you will face.
	</p>

   #### [Binary Tabular Data Classification with PySpark (Tabular Data)](https://github.com/hyunjoonbok/PySpark/blob/master/Binary%20Tabular%20Data%20Classification%20with%20PySpark.ipynb) 
   <p>
    This notebook covers a classification problem in Machine Learning and go through a comprehensive guide to succesfully develop an End-to-End ML class prediction model using PySpark. We will use a number of different supervised algorithms to precisely predict individuals’ income using data collected from the 1994 U.S. Census. We will then choose the best candidate algorithm from preliminary results and further optimize this algorithm to best model the data. Our goal with this implementation is to build a model that accurately predicts whether an individual makes more than $50,000
	</p>
  
   #### [End-to-End Binary Classification ML Model with PySpark and MLlib (1)](https://github.com/hyunjoonbok/PySpark/blob/master/End-to-End%20Machine%20Learning%20Model%20using%20PySpark%20and%20MLlib.ipynb) 
   <p>
    In-Memory computation and Parallel-Processing are some of the major reasons that Apache Spark has become very popular in the big data industry to deal with data products at large scale and perform faster analysis. we are going to use a real world dataset from Home Credit Default Risk competition on kaggle. The target variable is either 0 (applicants who were able to pay back their loans)or 1 (applicants who were NOT able to pay back their loans). it is a binary classification problem with a highly imbalanced target label.
	</p>

   #### [End-to-End Binary Classification ML Model with PySpark and MLlib (2)](https://github.com/hyunjoonbok/PySpark/blob/master/End-to-End%20Machine%20Learning%20Model%20using%20PySpark%20and%20MLlib%20(2).ipynb) 
   <p>
    Machine learning in the real world is messy. Data sources contain missing values, include redundant rows, or may not fit in memory. Feature engineering often requires domain expertise and can be tedious. Modeling too often mixes data science and systems engineering, requiring not only knowledge of algorithms but also of machine architecture and distributed systems. In this notebook, we build a model to predict the quality of Portugese "Vinho Verde" wine based on the wine's physicochemical properties. It covers data importing, visualization, parallel hyperparameter computation, Explore the best performing model in MLflow, etc.
	</p>
		
  
   #### [Multi-class Text Classification Problem with PySpark and MLlib](https://github.com/hyunjoonbok/PySpark/blob/master/Multi-class%20Text%20Classification%20Problem%20with%20PySpark%20and%20MLlib.ipynb) 
   <p>
    Apache Spark is quickly gaining steam both in the headlines and real-world adoption, mainly because of its ability to process streaming data. With so much data being processed on a daily basis, it has become essential for us to be able to stream and analyze it in real time. We use Spark Machine Learning Library (Spark MLlib) to solve multi-class text classification problem
	</p>  
	
   #### [Multi-class classification using Decision Tree Problem with PySpark](https://github.com/hyunjoonbok/PySpark/blob/master/Multi-class%20classification%20using%20Decision%20Tree%20Problem%20with%20PySpark%20.ipynb) 
   <p>
    This notebook covers a full multi class classification problem with Decision Tree method to look at the SFO airport data to predict which customer to give the overall rating. It covers a complete cycle of modeling (data loadgin, create a model, evaludate a model, feature importance). 
	</p>  
	
   #### [Setting up Fast Hyperparameter Search Framework with Pyspark](https://github.com/hyunjoonbok/PySpark/blob/master/Setting%20up%20Fast%20Hyperparameter%20Search%20Framework%20with%20Pyspark.ipynb) 
   <p>
    In this notebook, we set up hyperparameter tuning framework in PySpark using machine learning libraries like scikit-learn/xgboost/lightgbm. Usually manual tuning has to change a lot of parameters. Hyperopt works only one model at a time. So it was taking up a lot of time to train each model and I was pretty short on time. But what if we can parallelize my model hyperparameter search process? We can choose to load your data using Spark, but here I start by creating our own classification data to set up a minimal example which we can work with.rt data to predict which customer to give the overall rating. It covers a complete cycle of modeling (data loadgin, create a model, evaludate a model, feature importance). 
	</p> 	

   #### [PySpark Know-How in Pratice(Advanced)](https://github.com/hyunjoonbok/PySpark/blob/master/%5BAdvanced%5D%20Spark%20Know-How%20in%20Pratice%20.ipynb) 
   <p>
   In this notebook, there would be a lot of advanced Spark Tips introduced that can be applied to boost the data processing. We go over two important method to increase performance and reduce cost: Re-partitioning and Coalesce. Parallelism allows to perform millions tasks simultaneosly on numerous number of machines in a cluster independently. Under the hood, each dataframe (RDD) is stored in partitions on different cluster nodes. 
	</p> 	

   #### [5 Spark Tips that will get you to another level(Advanced)](https://github.com/hyunjoonbok/PySpark/blob/master/%5BAdvanced%5D%205%20Spark%20Tips%20that%20will%20get%20you%20to%20another%20level.ipynb) 
   <p>
    The advanced (5) tips that will make you the master of Spark is here. Make sure to not slip any of it! 
	</p> 	



<hr>

## Contact
Created by [@hyunjoonbok](https://www.linkedin.com/in/hyunjoonbok/) - feel free to contact me!


## Resource 
- Ultimate PySpark Cheat Sheet [Blog](https://towardsdatascience.com/ultimate-pyspark-cheat-sheet-7d3938d13421)
- Use Apache Arrow to Assist PySpark in Data Processing [Medium](https://medium.com/datadriveninvestor/use-apache-arrow-to-assist-pyspark-in-data-processing-6c1cce134306)
- Real Python [Website](https://realpython.com/)
- Luminousmen Blog [Blog](https://luminousmen.com/)


## Reference 
- Victor Romain's [Medium](https://towardsdatascience.com/@rromanss23?source=post_page-----485fb3c94e5e----------------------)
- Official PySpark Documentation [Link](https://spark.apache.org/docs/latest/api/python/index.html)
