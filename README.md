Maven project example with AspectJ
=====================

Project example with [AspectJ](https://eclipse.org/aspectj/) and [Maven](http://maven.apache.org).

Load-time weaving

### Run ###
```
mvn compile exec:exec
```

### Create executable jar with dependencies ###
```
mvn package assembly:single
```

### Run jar from command-line ###
```
mvn clean package
cd target
java -javaagent:lib/aspectjweaver-1.8.5.jar -cp "aspectj-maven-example-0.1-SNAPSHOT-core.jar;aspectj-maven-example-0.1-SNAPSHOT-aop-only.jar" li.barlog.asjex.App
```
