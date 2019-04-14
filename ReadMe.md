# *Software Measurement Project (SOEN 6611)*
-------------------------------------------------------

The aim of this project is to calculate several software metrices and to define correlation between them.

### Professor: Jinqiu Yang

## Team Member Details

| Name | Student ID | Email ID |
| --- | --- | --- |
| Nirav Ashvinkumar Patel | 40081268 | niravjdn@gmail.com |
| Himansi Patel | 40072262 | himansipatel1994@gmail.com |
| Krishnan Krishnamoorthy | 40089054 |krish27794@gmail.com |
| Darwin Anirudh Godavari | 40093368 | darwinanirudh@gmail.com |
| Jayaprakash Kumar | 40083709 | jayaprakash6034@gmail.com |

## We calculated following metrices.

1. **Statement Coverage:** Statement coverage is a white box testing technique, which involves the execution of all the statements at least once in the source code. It is a metric, which is used to calculate and measure the number of statements in the source code which have been executed.
2. **Branch Coverage:** ranch coverage is a testing method, which aims to ensure that each one of the possible branch from each decision point is executed at least once and thereby ensuring that all reachable code is executed.
3. **Mutation Score:** Mutation testing is used to design new software tests and evaluate the quality of existing software tests.
4. **Cyclomatic Complexity:** Cyclomatic complexity is a software metric used to indicate the complexity of a program. It is a quantitative measure of the number of linearly independent paths through a program's source code. 
5. **Relative Code Churn** Code churn is a measure of the amount of code change taking place within a software unit over time.
6. **Software Defect Density**


## Selected Open-Source Systems

1. **Apache Common Collections** - [*project details*](https://commons.apache.org/proper/commons-collections/) , [*source-code*](https://github.com/apache/commons-collections) 
2. **Apache Commons Configuration** - [*project details*](https://commons.apache.org/proper/commons-configuration/) , [*source-code*](https://github.com/apache/commons-configuration) 
3. **Apache Commons Math** - [*project details*](http://commons.apache.org/proper/commons-math/) , [*source-code*](https://github.com/apache/commons-math) 
4. **Apache Commons IO** - [*project details*](https://commons.apache.org/proper/commons-io/) , [*source-code*](https://github.com/apache/commons-io) 
5. **Apache Commons Lang** - [*project details*](https://commons.apache.org/proper/commons-lang/) , [*source-code*](https://github.com/apache/commons-lang) 

## Directory Structure

    .                                   
    ├── Presentation         # Presentaion of the project - 4th April, 2019
    ├── Proposal]            # Proposal of the project
    ├── assets]              # Images or other screenshots
    ├── Data                 # Raw Data - CSV, HTML (All Metrics)
    ├── Jupyter Notebook     # Jupyter Notebook Source Code
    └── README.md

## Used tools for different metrices :

### CLOC - Counting lines of the program 

CLOC TUTORIAL

https://www.youtube.com/watch?v=QxiXKZftJRw&t=161s

Effectively count lines grouped by programming languages - http://cloc.sourceforge.net/

![CLOC - Output in Console](https://github.com/niravjdn/Software-Measurement-Project/blob/master/assets/cloc/cloc.jpg)

### Jacoco 

Code Coverage - https://www.eclemma.org/jacoco/

Added Dependency Plugin in pom.xml for PIT Test as below

```
<?xml version="1.0" encoding="UTF-8"?>
<plugin>
   <groupId>org.jacoco</groupId>
   <artifactId>jacoco-maven-plugin</artifactId>
   <version>0.7.7.201606060606</version>
   <executions>
      <execution>
         <goals>
            <goal>prepare-agent</goal>
         </goals>
      </execution>
      <execution>
         <id>report</id>
         <phase>prepare-package</phase>
         <goals>
            <goal>report</goal>
         </goals>
      </execution>
   </executions>
</plugin>
```

### How did we run Jacoco for our project

### PIT - Mutation Testing 

http://pitest.org/

http://pitest.org/quickstart/basic_concepts/

https://www.mkyong.com/maven/maven-pitest-mutation-testing-example/

http://pages.cs.aueb.gr/~kintism/papers/emse2017/

https://www.youtube.com/watch?v=wZeZMtqVmck&feature=youtu.be

### How did we run for PIT Tool for our project

Added Dependency Plugin in pom.xml for PIT Test as below

We didn't configure it for only certains classes, instead we ran it on entire project.On an average, It took 1-2 hours for 4 projects(collections, configurations, io, lang) and 8.5 hours for math.

Find the screenshot below.

![Apache-Commons-Math PIT Testing Time](https://github.com/niravjdn/Software-Measurement-Project/blob/master/assets/pit/math.jpg)

```
<plugin>
        <groupId>org.pitest</groupId>
        <artifactId>pitest-maven</artifactId>
        <version>LATEST</version>
        <configuration>
            <outputFormats>
                <param>HTML</param>
                <param>CSV</param>
            </outputFormats>
        </configuration>
</plugin>
```
Reference : http://pitest.org/quickstart/maven/

Following command to compile and run unit tests

```
mvn clean install
```

Following command to run PIT Test

```
mvn org.pitest:pitest-maven:mutationCoverage -X
```

X is for debug mode so we can see what's going on.

### Maven Installation Locally

https://maven.apache.org/install.html

### Some Maven Reference To Solve Errors While Compiling

Maven  Extension
https://github.com/objectledge/maven-extensions

m2e
http://grumpyapache.blogspot.com/2011/08/mess-that-is-m2e-connectors.html

### Correlation Reference (Python and Panda)

https://www.datascience.com/blog/introduction-to-correlation-learn-data-science-tutorials

### Data

http://smproject.techfunda.tk/

All generated data in can be found on above site as well.

### Hosting

If you want to explore this project, you can clone this project and open index.html(in data directory), or directly paste data directory to your sever hosting directory.


### Steps to find Commit ID for all the open source project that we were analyzed

Link : https://streamable.com/6ym1q

### Spearman's Rank order Correlation 

Spearman correlation calculation procedure were all explained here in  URL.

Link: https://statistics.laerd.com/statistical-guides/spearmans-rank-order-correlation-statistical-guide.php

Link: https://stackoverflow.com/questions/25571882/pandas-columns-correlation-with-statistical-significance

Link: https://geographyfieldwork.com/SpearmansRankCalculator.html

Link: https://data-flair.training/blogs/python-statistics/

### Metric 5 Calculation (Defect Density)

[Collected Data](https://docs.google.com/spreadsheets/d/1OLc574O0LQwj4k8kOsbQ10hUkA9bAmiEJ_5mA1jgC5g/edit?usp=sharing)

[Video](https://streamable.com/819kk)

### Metric 6 Calculation (Relative Churned Code)

[*Step 1 (Video)*](https://streamable.com/vabz9) 

[*Step 2 (Video)*](https://streamable.com/malqv) 

#### CLOC Usage guide for calculating relative code churn

```
cloc --diff file1.zip file2.zip
```
![CLOC usage for calculating difference between two files](https://github.com/niravjdn/Software-Measurement-Project/blob/master/assets/cloc-diff/cloc-diff.jpg)

### Jupyter Notebook

https://drive.google.com/open?id=1kB3hoNvKrX-gr6AuuCWKLyCX2E-MSnBL
