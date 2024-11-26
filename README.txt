This archetype allows you to generate a template for a web application that uses Apache Click, based on the sample web application.

Create a project NOW using the remote repository

 mvn archetype:create -DarchetypeGroupId=com.gilbertoca.archetypes \
    -DarchetypeArtifactId=click-archetype \
    -DarchetypeVersion=1.1-SNAPSHOT \
    -DremoteRepositories=http://github.com/gilberoca/maven2/ \
    -DgroupId=myGroupId \
    -DartifactId=myArtifactId    

Installing the Archetype locally

Download the click-archetype-1.1-SNAPSHOT.jar file.

Then install it into your local repository:

 mvn install:install-file \
   -DarchetypeGroupId=com.gilbertoca.archetypes \
   -DarchetypeArtifactId=click-archetype \
   -DarchetypeVersion=1.1-SNAPSHOT \
   -Dpackaging=jar 
   -Dfile=PATH_TO_JAR_YOU_DOWNLOADED/click-archetype-1.1-SNAPSHOT.jar

Getting and building the archetype locally

Download the Maven Archetype Click source:
git clone http://github.com/gilberoca/click-archetype

Navigate to the root folder and install the archetype locally with the following command:
cd click-archetype/
mvn install

Using the Archetype (if it's already installed locally)

Once you have access to the archetype, you use it as you would any other Maven archetype to create a template/stub project.
 
mvn archetype:generate \
   -DarchetypeGroupId=com.gilbertoca.archetypes \
   -DarchetypeArtifactId=click-archetype \
   -DarchetypeVersion=1.1-SNAPSHOT \
   -DgroupId=com.mycompany \
   -DartifactId=starweb \
   -DarchetypeCatalog=local

Running the sample webapp

After that you can move to the new project(starweb), test or run it:
cd starweb/
mvn jetty:run

To try the sample webapp, point your browser to http://localhost:8080.

or

mvn test