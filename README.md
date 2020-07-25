# Databases

* [Introduction to Database Systems]()
* [Sorting, Hashing and Single Table Queries]()
* [Lab: Implementing a Query Executor]()
* [Lab: Implementing a File Format]()
* [Indexes]()
* [Joins]()
* [The Relational Model and Query Optimization]()
* [Concurrency]()
* [Column Stores]()
* [Log-Structured Merge Trees]()
* [Distributed Databases]()
* [Case Study]()

***

## Introduction

Most businesses store data, and most of those do so in a sophisticated database
system. Better database engines have lead to increased business capabilities, so
a few decades of market pressure has lead to highly capable, complex systems.
But with great power comes great responsibility: misunderstanding database
engines can be costly. This course provides a first look under the hood of
database systems, to help give you the understanding needed to make wise
choices.

## Recommended Resources

We cover a lot of ground in this course, so its important that you complete the
prework. We have done our best to keep it as short and focused as possible, so
as to leave you with enough time to also work on your project. If any of the
prework appears excessive, please ask us for clarification around where to focus
your attention.

Much of the prework draws from a series of video lectures from the [Spring 2015
session of
CS186](https://archive.org/details/UCBerkeley_Course_Computer_Science_186), Joe Hellerstein’s databases course at Berkeley. We agree with
past students of this course that Professor Hellerstein does an exceptional job
of presenting the important high level concepts in database systems. Watching
the lectures before class will give us more time to consolidate these concepts
and extend them to our work and projects.

One unfortunate aspect of studying databases is that their are few good
textbooks: those best placed to write great textbooks seem to be starting
databases companies or taking lucrative positions in industry instead! As such,
much of our suggested reading will be in the form of papers.

The one textbook we do reference is [Database Management Systems](https://smile.amazon.com/Database-Management-Systems-Raghu-Ramakrishnan/dp/0072465638/) by Ramakrishnan
and Gehrke (R&G below). It is dated and often hard to follow, but it is
sometimes more approachable than papers on the topic. Chapter numbers are for
the third edition.

Many of our selected papers are [from the databases “Red
Book”](http://www.redbook.io/), a collection of
papers compiled and edited by Peter Bailis, Joe Hellerstein and Michael
Stonebraker. It is a good source for more advanced papers beyond those suggested
below.

> Database Management Systems by Ramakrishnan and Gehrke is one of the more
popular undergraduate-level databases textbooks. It leaves a lot to be desired
but some students have found it helpful as a supplement to our assigned
prework. It is used at Berkeley and occasionally referenced in the CS186
lectures.An alternative textbook is Database Systems: The Complete Book by Hector
Garcia-Molina, Jeffrey D. Ullman and Jennifer Widom based on their course at
Stanford. In both cases, we’d only suggest investing in one of these books if you
particularly prefer textbooks over the material we’ve linked in the assigned
prework.

## Course Exercises

Prior iterations of the course involved an ongoing project to build a simple
relational database management system from scratch. Although some past students
have found this project to be one of the highlights of this course, we’ve also
encountered some challenges in structuring the course around such a project.

This time, we will instead take a more targeted approach, with exercises that
emphasize particularly interesting or educational components of a database
system. However, if you’re still interested in building a simple database that
works end-to-end, the two “Lab” sessions will cover most of the core
functionality, and several subsequent sessions (e.g. Indexes, Joins) will
suggest optional additional project steps.

For course exercises, our recommended approach is:

* Consult prework readings or videos to develop a basic understanding of the topic;
* Try to complete the exercise on your own, but make a note of any difficulties if you get stuck;
* Attend class to discuss the general principles, your own approach, and any difficulties encountered; then,
* Revisit and complete the exercise after class.

To address some frequently asked questions: it’s preferable to work in pairs if
possible, but up to you; you should use the language with which you’re most
comfortable; your instructor will be more than happy to provide detailed code
review, but this is optional; and, we will often start by going around the room
to discuss progress and difficulties encountered.
