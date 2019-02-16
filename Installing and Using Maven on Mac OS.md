# Installing Maven

Very helpful YouTube video here:  https://www.youtube.com/watch?v=j0OnSAP-KtU&vl=en

1.  Download Maven .gz file from maven.apache.org

2.  Create a .bash_profile file in home directory

3.  Put the following lines in the .bash_profile file:

export M2_HOME=/Applications/apache-maven-3.4.5
export PATH=$PATH:$M2_HOME/bin

4.  Reload the .bash_profile file using the source command:  source .bash_profile

5.  Test to see if Maven is loaded:  mvn - version


Instructions from the YouTube video:
Download the Apache Maven bin.tar.gz file from http://maven.apache.org/download.cgi.
Extract the distribution archive to  /Applications/apache-maven-3.4.5.

$ tar -xvf apache-maven-3.4.5-bin.tar.gz

Add the M2_HOME environment variable. Edit your ~/.bash_profile 

open -e ~/.bash_profile

Add the following exports

export M2_HOME=/Applications/apache-maven-3.4.5
export PATH=$PATH:$M2_HOME/bin


# Using Maven

1.  Add the following dependencies to the pom.xml

        <dependencies>
                <dependency>
                        <groupId>junit</groupId>
                        <artifactId>junit</artifactId>
                        <version>4.13-beta-1</version>
                        <scope>test</scope>
                </dependency>
                <dependency>
                    <groupId>org.hamcrest</groupId>
                    <artifactId>hamcrest-all</artifactId>
                    <version>1.3</version>
                </dependency>
        </dependencies>

2.  Add the following properties to the pom.xml

        <properties>
                <maven.compiler.source>1.6</maven.compiler.source>
                <maven.compiler.target>1.6</maven.compiler.target>
        </properties>

3.  Make sure the following plugin is documented in the pom.xml

          <plugin>
                <!-- Build an executable JAR -->
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-jar-plugin</artifactId>
                <version>3.1.0</version>
                <configuration>
                    <archive>
                        <manifest>
                            <addClasspath>true</addClasspath>
                            <classpathPrefix>lib/</classpathPrefix>
                            <mainClass>com.pluralsight.testing.m2.Main</mainClass> (name of primary method to run)
                        </manifest>
                    </archive>
                </configuration>
            </plugin>

4.  To compile and run tests:  mvn clean test

5.  To compile, run tests, and build .jar file in the \target directory:  mvn clean package

6.  Run the jar file:  java -jar target/demo-1.0-SNAPSHOT.jar


