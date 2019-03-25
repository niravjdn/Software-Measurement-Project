## *This is the Software Measurement Project (SOEN 6611)*

Used tools for different metrices :

## CLOC - Counting lines of the program 

effectively count lines grouped by programming languages - http://cloc.sourceforge.net/

## Jacoco - Code Coverage - https://www.eclemma.org/jacoco/

## PIT - Mutation Testing 

http://pitest.org/

https://www.mkyong.com/maven/maven-pitest-mutation-testing-example/

http://pages.cs.aueb.gr/~kintism/papers/emse2017/

### How did we run for our project

Added Dependency Plugin in pom.xml for PITest as below

We didn't configure it for only certains classes, instead we ran it on entire project. It took more than 2 hours for some projects. On an average, It took 1-3 hours.

```
<plugin>
    <groupId>org.pitest</groupId>
    <artifactId>pitest-maven</artifactId>
    <version>LATEST</version>
 </plugin>
```
Reference : http://pitest.org/quickstart/maven/

Following command to compile and run unit tests

```
mvn clean install
```

Following command to run PI Test

```
mvn org.pitest:pitest-maven:mutationCoverage -X
```

X is for debug mode so we can see what's going on.

## Maven Installation Locally

https://maven.apache.org/install.html

## Some Maven Reference To Solve Errors While Compiling

Maven  Extension
https://github.com/objectledge/maven-extensions

m2e
http://grumpyapache.blogspot.com/2011/08/mess-that-is-m2e-connectors.html

## Correlation Reference (Python and Panda)

https://www.datascience.com/blog/introduction-to-correlation-learn-data-science-tutorials

## Data
http://smproject.techfunda.tk/