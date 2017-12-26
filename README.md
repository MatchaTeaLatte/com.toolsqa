# com.toolsqa

This is a sample Software Test Automation Framework built as a Maven Project and
applying Behavior Driven Development principles with Cucumber and Junit. The code is written in Java language. 
Selenium WebDriver is used for executing test case.

Here is a project hierarchy :

         com.toolsqa
              src/test/java
                      com.toolsqa.pages
                      runners
                      stepDefinitions
                      utilities
              src/test/resources
                      driver
                      features
                      test_data
              target
              pom.xml
              readMe
          

src/test/java: this folder is for the classes where I define my automation script implementation.

--> com.toolsqa.pages folder consists of java class which plays a role as object repository for web UI elements and 
also contains Page methods which perform operations on those WebElements. This approach is called Page Object Model which helps make the code more readable, maintainable, and reusable.

--> runners folder has a Runner class which is responsible for executing my test. 
@RunWith annotation tells JUnit that tests should run using Cucumber class present in ‘Cucumber.api.junit‘ package.
@CucumberOptions basically provides the same options as the cucumber jvm command line.So, we can specify the path to feature files, 
path to step definitions, if we want to run the execution in dry mode or not etc.

--> stepDefinitions folder consists of two classes. 1.Step Definitions is for implemented steps of the scenario we have in the cucumber feature file.
2. Hook is a block of code that runs before or after each scenario. 
This class allows us to better manage the code workflow and helps us to reduce the code redundancy. 

--> utilities folder is for my utility classes which consist of reusable methods which are created once there and can be used as many times as I want through out the development cycle.

scr/test/resources: This folder is for any related resources for the development like driver, cucumber feature files and test data.

--> driver folder contains the driver needed for my framework.

--> features folder consists of cucumber feature files where I define my unimplemented scenarios written in Gherkin language. By doing this, 
I'm making sure that my scenarios are described understandable to my non technical team and stakeholders.

--> properties folder is for defining the properties needed for the framework.

--> JRE system library and  Maven dependencies are for the system jar files of Java and other dependencies that I needed for my framework.

--> target folder contains report.json report file generated after execution of the script so that I can come up with test pass/ fail reports in a pretty format.


--> pom.xml is a file where I define the dependencies needed for my framework's development cycle.

That's pretty much how the structure of my framework looks like.
And in order to run the code, 
		--> import the code into eclipse
				 --> update the maven project 
				 		-->please, make sure that browser and WebDriver are updated to latest version.
For Mac os, please change to Config.getProperty("macChrome").
  	    --> go to the runner class
  	    --> run the class as Junit test.
  	    --> then go to target folder after execution,find the html report which basically tells what steps are
  	    	 passed and what are failed with embeded screenShot in the report.

Thank you!!
 
