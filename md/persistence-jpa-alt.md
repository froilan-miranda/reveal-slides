# JPA
## Java Persistance API

-
-

* Introduction
* Underand Java Persistence API
* Mapping and manage enitites
* Querying entitites
* Relationships and hineritance
* Lifecycle and callbacks

-
-

## Usage of Java Persistence API

* Simple Applications
* Complex Applications
* Cloud
* Relational Databases only

-
-

## What is persistence?

* Data
* Storage
* Central point or applications
* Mainpulating data
* Relational databases

-
-

## Manipulating Persisted Data without JPA

Objects - to hold data in our applictions

Relational databases - to store data

Object-relational mapping - process of mapping objects to records of a table 

ORM's are not standard to java, so it leads us to relying on external frameworks or low level JDBC API's

-

### JDBC

* Java Database Connectivity
* Java-based data access technology
* Methods for querying and updateing data
* Robust
* Low level and verbose

-

### Disadvantages

* SQL is not Java
* JDBC is a low level API
* SQL is not easy to refactor
* JDBC is verbose
* Hard to read
* Hard to maintain

-

### Manipulating Persisted Data with JPA

* Standard
* Object-relational mapping
* Meta-data mapping
* Removes boiler plate code
* Simple api for CRUD
* Object oriented query language


-

### Advantages of JPA

* No manual mapping
* no sql satements
* Interaction through Entity Manager
* non intrusive
* lightweight
* elegant api
* powerful

-
-

## Understanding Java Persistance API

-

### What is a database

* organized collection of data
* model our business requirements
* process information
* files 
* schema-less
* relational databases

-

### What is a relational database

* Collection of tables
* Row
* Columns
* Relationships
* Identity through primary keys

-

### What is Object Oriented Programming

* Objects
* Classes
* Inheritance
* reference to other classes 
* Abstract classes, interfaces, enumerations
* Encpsulate state and behavior

-

### What is Object Relational Mapping

* Bring relational databases and objects together
* Objects have transient state
* Relational databases store state
* Mapping between objects and tables
* Java persistence API

-

### What is Java Persistence API

* Abstraction above JDBC
* ORM
* Entity Manager
	* CRUD operations
	* Java Persistence Query Language
* Transactions

-

### What JPA is not

* Schema-less databases
* NoSQL
* JSON
* XML
* JPQL != SQL

-

### JPA Spec

* Specification
* Java Community Process
* Java Specification Request

-

### JPA Implementations

* EclipseLink
* Hibernate
* Open JPA

-

### JPA Packages

```
javax.persistence
javax.persistence.criteria
javax.persistence.metamodel
javax.perisstence.spi
```

-

### Mapping Metadata

Mapping of object data to database data is managed with annotations

* @Entity
* @Id
* @Column

There is a large library of annotations to choose from

-

### CRUD Operations

An EntityManager makes available an interface for executing CRUD operations. A EntityManagerFactory supplies EntityMangers

-

### Where to use JPA

Because of JPA's non-intrusive style it can be used in all parts of a program

* Client
* Business logic
* Model

-
-

## JPA - Mangage Entities

The Enitity Manger is responsible for persisting Enitities to the database. The Enitiy Manager uses references from the persistence unit to connect to the database

-

### Persistence unit

Found in the persistance.xml, this sets all the properties needed to connect with the database allowing the Entity manager to interact with the database

-

### CRUD Operatioins on an Entity

* persist()
* find()
* remove()

-

### Transactions

* Consistent State
* Changes succeed or fail atomically
* Transactional operations
	* Persist
	* Remove
	* Update
* Find can be non-transactional
* EntityTransaction

-

### Default Entity Mapping

`@javax.persistence.Entity` - Tells JPA that this is a class to be persisted and not a regular class.

`@javax.persistence.Id` - Identifies the unique identifier for the object to mapped as primary key of data record

* No-arg constructor
* getters and setters
* Concrete or abstract class
* Enums or interfaces cannot be entities

-

### Highly Opinionated

Convention over configuration

JPA provider applies the default rules

Entity name -> Table name

Attribute name -> Column name

JDBC rules for mapping primitives

String -> VARCHAR(255)
Long -> BIGINT
BOOLEAN -> SMALLINT
...

-

### Customizing Table

* @Table(name = "SomeTableName")
* @GeneratedValue(stratagy.GenerationType.AUTO)
* @Column(name="SomeColumnName")
* @Transient

And many more






























