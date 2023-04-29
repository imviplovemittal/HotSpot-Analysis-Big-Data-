# HotSpot-Analysis [Big Data]

### Version history
v1.1, Nov 16, Fix a bug in "Entrace.scala"
v1.0, Nov 13, Initial version

A spatial hot spot analysis project that performs two different tasks: Hot Zone Analysis and Hot Cell Analysis using Apache Spark.

## Table of Contents
- Introduction
- Requirements
- Installation
- Usage
- Sample Output
- License
- Introduction

This project is focused on applying spatial statistics to spatio-temporal big data to identify statistically significant spatial hot spots using Apache Spark. The project includes two different tasks: Hot Zone Analysis and Hot Cell Analysis.

## Requirements
- Scala 2.11
- Apache Spark 2.4.0
- sbt 1.3.0

## Installation
Clone the repository
```git clone https://github.com/imviplovemittal/HotSpot-Analysis-Big-Data-.git```
Change to the project directory
cd HotSpot-Analysis-Big-Data-

## Usage
Compile the project
```sbt clean assembly```

Find the packaged jar in "./target/scala-2.11/cse512-hotspot-analysis-template_2.11-0.1.0.jar"
Submit the jar to Spark using the Spark command "./bin/spark-submit"

```./bin/spark-submit ./target/scala-2.11/cse512-hotspot-analysis-template_2.11-0.1.0.jar output/path hotzoneanalysis point-data/path zone-data/path hotcellanalysis yellow_tripdata/path```

## Sample Output
### Hot Zone Analysis
All zones with their count, sorted by "rectangle" string in an ascending order.

```
"-73.795658,40.743334,-73.753772,40.779114",1
"-73.797297,40.738291,-73.775740,40.770411",1
"-73.832707,40.620010,-73.746541,40.665414",20
```

### Hot Cell Analysis
The coordinates of the top 50 hottest cells sorted by their G score in a descending order. Note, DO NOT OUTPUT G score.

```
-7399,4075,15
-7399,4075,29
-7399,4075,22
```

## License
This project is licensed under the MIT License - see the LICENSE file for details.
