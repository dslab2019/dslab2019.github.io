
# DSLab Week 8

## Week 2/3: Spark DataFrames

---

An API for computing with structured data (if it's a table, it fits)

Some key points:

* does not require using basic RDD methods (`map`, `reduce` etc.)
* for many common operations data in a DataFrame follows a specified "schema" that tells Spark which kinds of data are in each column
* the basic data unit is a `Row` which contains a value for each of the columns
* automatically read data from a variety of formats, e.g. json, parquet, some database formats (through plugins)
* can give some nice performance improvements!
* Spark can optimize the execution because it knows more about the data layout
* most of the work can take place in the JVM without need to ship to python
* operations can be 'pushed down' to the optimized DB layer, e.g. filtering

--

## [DataFrame demo](./dataframe_demo.slides.html)

### [Download the notebook](./dataframe_demo.ipynb)

--

## PySpark architecture overview

<img src="figs/pyspark_architecture.png" height=500px>


* Spark workers pull data from sources into the JVM
* Data is actually processed in python subprocesses
* (De)Serialization and streaming at every step


--

## PySpark DataFrame optimization

<img src="figs/databricks_catalyst.png" height=200px>

* By typing the data and using built-in functions, operations can be optimized
* Certain operations (e.g. filtering) can be pushed one lever lower (to the DB for example)
* In the end, still runs on RDD - can always resort to the lower-level API

--

## Useful Links

* [Lab repository](https://git-dslab.epfl.ch/dslab2019/week8-spark-dataframes)
* [A nice post about DataFrames and code generation](https://virtuslab.com/blog/spark-sql-hood-part-i/)
* [General Spark docs](http://spark.apache.org/docs/latest)
* [Spark DataFrame intro (good for a lookup of basic syntax)](http://spark.apache.org/docs/latest/sql-programming-guide.html)
* [Spark DataFrame Reference](http://spark.apache.org/docs/latest/api/python/pyspark.sql.html)
* [Spark ML Reference](http://spark.apache.org/docs/latest/api/python/pyspark.ml#pyspark-ml-package)
