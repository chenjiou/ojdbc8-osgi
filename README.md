OSGi wrapper for Oracle Database 12.2.0.1 JDBC Driver (Java 8)
==============================================

Overview
--------

This Maven project produces OSGi wrapper for Oracle Database 12.2.0.1 JDBC Driver for use with Oracle Java 8.

Build instructions
------------------

The build depends on the official Oracle JDBC driver JAR file provided by [Oracle](http://www.oracle.com/technetwork/database/features/jdbc/jdbc-ucp-122-3110062.html). 

For example to build the bundle for the Oracle JDBC driver for Java 1.6, follow the steps below.

1. Download the desired driver JAR file for [Oracle 12c](http://www.oracle.com/technetwork/database/features/jdbc/jdbc-ucp-122-3110062.html) and Java 8.
2. Edit the POM to reflect the Oracle RDBMS version.
3. Install the driver to the local Maven repository.

        mvn install:install-file -Dfile=ojdbc8.jar -DgroupId=com.oracle -DartifactId=ojdbc8 -Dversion=12.2.0.1 -Dpackaging=jar

4. Build and install the OSGi wrapped driver bundle.

        mvn install

Licensing
---------

This Maven build script is licensed under the terms contained in the file named "LICENSE.txt" in this directory.
