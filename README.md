OSGi wrapper for Oracle JDBC driver (Java 1.6)
==============================================

Overview
--------

This Maven project produces OSGi bundle wrappers for Oracle RDBMS JDBC drivers for use with Oracle Java 1.6.

Build instructions
------------------

The build depends on the official Oracle JDBC driver JAR file provided by [Oracle](http://www.oracle.com/technetwork/database/database-technologies/express-edition/overview/index.html). 

For example to build the bundle for the Oracle JDBC driver for Java 1.6, follow the steps below.

1. Download the desired driver JAR file for [Oracle 11gR2](http://www.oracle
.com/technetwork/database/enterprise-edition/jdbc-112010-090769.html) and Java 1.6.
2. Rename the file to ojdbc6.jar and move the file to the *ext* directory.
3. Edit the POM to reflect the Oracle RDBMS version.
4. Install the driver to the local Maven repository

        mvn install:install-file -Dfile=ext/ojdbc6.jar -DgroupId=com.oracle -DartifactId=ojdbc6 -Dversion=11.2.0.4 -Dpackaging=jar

5. Build and install the OSGi wrapped driver bundle

        mvn install

Licensing
---------

This Maven build script is licensed under the terms contained in the file named "LICENSE.txt" in this directory.
