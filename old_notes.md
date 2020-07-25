# Introduction to Database Systems

My work for the Berkeley CS186 Database Systems course.

## Introduction _1-20-2015_


## Database Design: Entity-Relationship Models _2-24-2015_

### Describing Data: Data Models

* Data Model: A collection of concepts for describing data. It is an abstraction.
* Schema: Description of a particular collection of data, using a given data model.
* Relational Model of data:
  * Main concept: relation (table), rows, columns
  * Every relation has a schema
    * Describes the columns
    * Column names and domains (data types)

The relational model occupies the middle ground between the very simple (ie using a key-value store) and the complex (ie a document store or json), where things are nested and you have to reason about trees.

### There are three levels of abstraction in a database:

![Three levels of Database Abstraction](https://github.com/paulghaddad/databases/blob/master/images/three_levels_of_abstraction.png)

Example:
 
* Conceptual Schema:
  - Students(sid text, name text, login text, age integer, gpa float)
  - Courses(cid text, cname text, credits integer)
  - Enrolled(sid text, cid text, grade text)
* Physical Schema:
  - Relations stored as unordered files
  - Index on first column of Students
* External Schema (View):
  - Course_Info(cid text, enrollment integer)
  
### Data Independence

* Insulate applications from structure of data
* Logical data independence:
  - Protection from changes in _logical_ structure.
* Physical data independence:
  - Protection from changes in _physical_ structure.
  
Key point: this is important because databases and their associated application persist, and normally at different rates:

`dapp/dt << denv/dt` => the rate of change of your application is normally much slower than the rate of rate of your environment. Thus we want to make them independent so we can change one without affecting the other.

### Data Models

* Connect concepts to bits.
* Many models exist
* We will focus on the relational model
  - clean and common
  - its a generalization of a simple key/value pairs
* The Entity-Relationship model is also handy for design
  - because it translates down to the Relational Model
  
Why focus on the relational model?
* Most widely used
* Other models exist (and co-exist)
  - Legacy systems in older models
  - Object-Relational mergers
    - OO features provided by DBMS
    - ORMs outside the DBMS
  - XML/JSON, etc
    - nested and semi-structured data
    - Most relational engines now handle these to a degree
    
### Entity-Relationship Model
 
  * Relational model is a great formalism and a clearn system framework
  * But it's a bit detailed at design time:
    * a bit fussy for brainstorming
    * hard to communicate to customers
  * Entity-Relationship model is a popular "shim" over the relational model
    * it's graphical and at a slightly higher level
   
#### Steps in Traditional DB Design (old style)
 
1. Requirements analysis
  * user needs; what must the db do?
2. Conceptual design
  * high level description (often doen with the ER model)
3. Logical design
  * translate ER into DBMS data model (translate classes to actual CREATE statements, ie in migrations)
4. Schema Refinement
  * consistency and normalization
5. Physical design: indexes, disk layout
6. Security design: who accesses what, and how?

#### Conceptual Design

* What are the entities and relationships?
* What info about E's and R's should be in the DB?
* What _integrity constraints_ (business rules) hold?
* The ER diagram is the "schema"
* Can map an ER diagram into a relational schema
* Conceptual design is where the software/data engineering begins, ie in constructing _models_.

#### Modern Pattern: "Schema on Use"

* What about more agile, less governed environments?
* Don't let the lack of schema prevent you from storing data
  * just use binary, text, CSV, JSON, etc
  * Can shove the data into a DBMS, or just a filesystem
  * Most database engines can query files directly these days
* Wrangle the data into shape _as needed_
  * Essentially defining views over the raw data
  * This amounts to database design, at the view level
  * What about integrity constraints?
    - Instead, define "anomoly indicator" columns to flag strange data -- or queries
* Fits well with read/append-only data (ie log files)
  * Eg, big data like Hadoop
  * Less of a fit with udpate-heavy data
* Analogous to strong vs. loose typing in programming languages

#### ER Model Basics

There are Entities and Relationships, that's it!

* Entity
  - A real-world object describes by a set of attribute values
  
* Entity Set: a collection of similar entities
  - ie, all employees
  - All entities in an entity set have the same attributes
  - Each entity set has a _key_ that defines uniquely a specific entity in the entity set
  - Each attribute has a _domain_ (data type)
  
![Employee ER Model]()

* Relationship: association among two or more entities.
  - Eg, Smith works in the Pharmacy department
  - relationships can have their own attributes
* Relationship Set: Collection of similar relationships
  - An n-ary relationship set `R` relates `n` entity sets `E1...En`; each relationship in `R` involves entities `e1 = E1, ... en = En`
  
Entities are represented by rectangles; attributes by circles; and relationships by diamonds.

![Employee-Departments ER Model]()
  
