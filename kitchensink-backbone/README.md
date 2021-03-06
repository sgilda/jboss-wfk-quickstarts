kitchensink-backbone: Shows how to use Backbone.js with JAX-RS and Java EE on JBoss
========================
Author: Joshua Wilson
Level: Intermediate
Technologies: Backbone, CDI, JPA, EJB, JPA, JAX-RS, BV
Summary: An example of Backbone.js integrated with jQuery, REST, and a Java back-end running on JBoss.
Target Product: WFK
Product Versions: EAP 6.1, EAP 6.2, WFK 2.4
Source: <https://github.com/jboss-developer/jboss-wfk-quickstarts/>

What is it?
-----------

This is your project! It is a sample, deployable Maven 3 project to help you get your foot in the door developing with 
Backbone.js on Java EE 6 on Red Hat JBoss Enterprise Application Platform 6.1 or later.

This project is setup to allow you to create a compliant Java EE 6 application using CDI 1.0, EJB 3.1, JPA 2.0 and Bean 
Validation 1.0. It includes a persistence unit and some sample persistence and transaction code to introduce you to 
database access in enterprise Java.

Backbone.js is a MVC for the browser.  That is to say, it has a Model (JavaScript/JSON objects that hold data), a View 
(HTML/Templates/CSS for display), and a Controller (JavaScript files that take commands from the screen and send them to 
the server and then return the results). 

All of the code using the Backbone.js library can be found in /src/main/webapp/js/app.js.  You will find the Model 
(and the Collection of the Model) there and the View where almost all the logic resides. 

System requirements
-------------------

The application this project produces is designed to be run on Red Hat JBoss Enterprise Application Platform (EAP) 6.1 or later with the Red Hat JBoss Web Framework Kit (WFK) 2.4.

All you need to build this project is Java 6.0 (Java SDK 1.6) or later, Maven 3.0 or later.

Configure Maven
---------------

If you have not yet done so, you must [Configure Maven](../README.md#configure-maven) before testing the quickstarts.


Start the JBoss Server
-------------------------

1. Open a command line and navigate to the root of the JBoss server directory.
2. The following shows the command line to start the server with the web profile:

        For Linux:   JBOSS_HOME/bin/standalone.sh
        For Windows: JBOSS_HOME\bin\standalone.bat


Build and Deploy the Quickstart
-------------------------

_NOTE: The following build command assumes you have configured your Maven user settings. If you have not, you must include 
Maven setting arguments on the command line. See [Build and Deploy the Quickstarts](../README.md#build-and-deploy-the-quickstarts) for 
complete instructions and additional options._

1. Make sure you have started the JBoss Server as described above.
2. Open a command line and navigate to the root directory of this quickstart.
3. Type this command to build and deploy the archive:

        mvn clean package jboss-as:deploy

4. This will deploy `target/jboss-kitchensink-backbone.war` to the running instance of the server.


Access the application
---------------------

The application will be running at the following URL: <http://localhost:8080/jboss-kitchensink-backbone/>.


Undeploy the Archive
--------------------

1. Make sure you have started the JBoss Server as described above.
2. Open a command line and navigate to the root directory of this quickstart.
3. When you are finished testing, type this command to undeploy the archive:

        mvn jboss-as:undeploy


Run the Arquillian Tests
-------------------------

This quickstart provides Arquillian tests. By default, these tests are configured to be skipped as Arquillian tests 
require the use of a container.

_NOTE: The following commands assume you have configured your Maven user settings. If you have not, you must include 
Maven setting arguments on the command line. See [Run the Arquillian Tests](../README.md#run-the-arquillian-tests) for complete 
instructions and additional options._

1. Make sure you have started the JBoss Server as described above.
2. Open a command line and navigate to the root directory of this quickstart.
3. Type the following command to run the test goal with the following profile activated:

        mvn clean test -Parq-jbossas-remote


Run the Quickstart in JBoss Developer Studio or Eclipse
-------------------------------------
You can also start the server and deploy the quickstarts from Eclipse using JBoss tools. For more information, see 
[Use JBoss Developer Studio or Eclipse to Run the Quickstarts](../README.md#use-jboss-developer-studio-or-eclipse-to-run-the-quickstarts)


Debug the Application
------------------------------------

If you want to debug the source code or look at the Javadocs of any library in the project, run either of the following 
commands to pull them into your local repository. The IDE should then detect them.

    mvn dependency:sources
    mvn dependency:resolve -Dclassifier=javadoc
