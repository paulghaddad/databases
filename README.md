# Introduction to Database Systems

My work for the Berkeley CS186 Database Systems course.

## Introduction (1-20-2015)



## Database Design: Entity-Relationship Models

Describing Data: Data Models

* Data Model: A collection of concepts for describing data. It is an abstraction.
* Schema: Description of a particular collection of data, using a given data model.
* Relational Model of data:
  * Main concept: relation (table), rows, columns
  * Every relation has a schema
    * Describes the columns
    * Column names and domains (data types)

The relational model occupies the middle ground between the very simple (ie using a key-value store) and the complex (ie a document store or json), where things are nested and you have to reason about trees.

There are three levels of abstraction in a database:

![Three levels of Database Abstraction](https://github.com/paulghaddad/dotfiles/blob/master/images/bradfield/apis/three_levels_of_abstraction.png)
