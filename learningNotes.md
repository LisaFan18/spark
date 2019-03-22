## QA about scala 
1. [difference between object and class in scala](https://stackoverflow.com/questions/1755345/difference-between-object-and-class-in-scala)

## QA about spark

## QA about others
1. [difference between Gradle and Maven](https://stackify.com/gradle-vs-maven/)

2. How to add a new dependency by Gradle?   
hw2_4 needs to use package breeze.linalg.{norm,DenseVector}, my spark project is set up by Gradle.   
* step1: follow scalanlp/breeze [installation instruction](https://github.com/scalanlp/breeze/wiki/Installation), scroll down to "other build tools" 
to find out the configuration of breeze in Gradle as below:  
```xml
// https://mvnrepository.com/artifact/org.scalanlp/breeze
compile group: 'org.scalanlp', name: 'breeze_2.10', version: '0.12'
```
* step2: copy and paste it to the dependencies component in the **build.gradle** configuration file.  
* step3: run **./gradlew idea** in terminal under the project path. the output looks like this: 
```xml
nbp-245-213:scala-spark-tutorial username$ ./gradlew idea
:ideaProject
Download https://repo1.maven.org/maven2/org/scalanlp/breeze_2.10/0.12/breeze_2.10-0.12.pom
Download https://repo1.maven.org/maven2/org/scalanlp/breeze-macros_2.10/0.12/breeze-macros_2.10-0.12.pom
...
Download https://repo1.maven.org/maven2/org/scalanlp/breeze_2.10/0.12/breeze_2.10-0.12.jar
Download https://repo1.maven.org/maven2/org/scalanlp/breeze-macros_2.10/0.12/breeze-macros_2.10-0.12.jar
...
:ideaModule
:ideaWorkspace
:idea

BUILD SUCCESSFUL
```
* step4: reload the intellij project and you'll find breeze_2.10-0.12.jar in the External Libraries



