# Database Connection

The `Database Connection` repository is part of a Java-based chat application project that allows users to communicate with each other through a simple chat interface. This README file specifically focuses on the database related files and classes that interact with the `Hyper SQL (HSQL)` database to perform `CRUD` operations.

> Disclaimer: The files and code present in the `Database Connection` repository is not the complete chat application, but only includes database files and classes that are essential to interact with the database. These files cannot be imported to use as a standalone chat application. 

## Table of Contents

- Database
  - Database.lck
  - Database.properties
  - Database.script
- Classes
  - Database.java
  - DatabaseFactory.java
  - HSQLDatabase.java
  - HSQLDatabaseTest.java

## Database

The `Database` folder in the `Database Connection` repository contains the following files:

- **Database.lck**: It is a lock file that is used to prevent multiple instances of the database from accessing it simultaneously.

- **Database.properties**: This file contains the properties of the database, such as the URL and user credentials.

- **Database.script**: This file contains the schema and data of the database.

These files are created by the `Hyper SQL (HSQL)` database and are used to manage the database.

## Classes

The following classes are present in the `src` folder under the `database` package:

 - **Database.java** : The `Database` class is an interface which acts like a super class. It defines the methods which should be implemented by the respective subclasses for interacting with the database. In this project, we only have one subclass, namely `HSQLDatabase.java`.

 - **DatabaseFactory.java**: The `DatabaseFactory` class implements the `factory design pattern` which is responsible for hiding the actual implementation. The DatabaseFactory class contains only one public method `getDatabase()` which creates and retrieves the `Singleton instance` of the `HSQLDatabase.java` class.

 - **HSQLDatabase.java**: The `HSQLDatabase` class implements the methods defined in the `Database` interface, providing the specific implementation for working with the Hyper SQL (HSQL) database. It also implements the "Singleton pattern" to ensure that only one instance of the class is created.

 - **HSQLDatabaseTest.java** : The `HSQLDatabaseTest` class contains the JUnit tests to ensure the methods in the `HSQLDatabase` class are working properly without any errors.