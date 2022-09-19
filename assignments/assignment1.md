# Assignment 1

## Stakeholders

- Customer: JAMK
- Management: Project management
- JAMK representative (and JAMK management)
- Developers
- Designers
- End user: Teachers and students of JAMK, librarians

## Feasibility study

Funds allocated from the client JAMK Central Management for the project is 300 000 €. Client expects complete design and development of the system.

The end product of the project will be a web application. It is required to have complete usability on computers as well as on mobile devices. As the end-users of the site will be students and teachers of JAMK, JAMK login credentials must be used for log in on the website. On the site, users can loan, reserve or extend the loan time of a book while logged in. Also new functionality for borrowing e-books must be included. 

Project will be a full stack development project with front- and back-end functionality. A database solution must be developed in order to save the data about the books, users, and loans. Security of the site is a high priority for the client as the user information must not be leaked under any circumstances. Robustness is expected as the max load of site will be in hundreds of simultaneous users.

In the usage of user data, European Union's General Data Protection Regulation must be considered.

Expected schedule of the project is still unclear.

## Software Requirement Specification

#### 1 Introduction

##### 1.1 Purpose

The purpose of this document is to build a library management system for replacing old the old system. Main reason for creating new solution is adding support for loaning e-books.

##### 1.2 Conventions

|DB|Database|
|FR|Functional Requirement|

##### 1.3 Intended audience

As the project is meant to be library management system for JAMK, the students and teachers of JAMK will be using it as well as librarians.

##### 1.4 Product scope

The product being developed in this project is a library management web application. It must be usable on computers and on mobile devices. The purpose of application is tracking the book loans. Users can make reservations, loans, and loan time extensions on the site. Also a functionality for loaning e-books is implemented. E-books will have loan periods like physical books. When the loan ends, user will have to lose rights to view the content afterwards. The system is used with JAMK's own log in credentials. Therefore the JAMK login system will have to be embedded on the site.


#### 2 Overall description

##### 2.1 Product perspective

Web page is a standalone application. However, JAMK's log in system must be integrated to website so the users can use their credentials for accessing the page.

##### 2.2 Product functions

- Making an reservation for a book
- Seeing the loan status of a book
- Loaning a book
- Loaning an e-book
- Extending loan time

![](/resources/assignment1/usecase.png)
Use case diagram

![](/resources/assignment1/sequencediagram.png)
Sequence diagram example of making loan

##### 2.3 Operating envinonment

- Database
- Server system
- DB
- Platform

##### 2.4 Design and implementation constraints

Constraint for the design is ease of usage. For the implementation, technical constraints must be considered when creating the application.

##### 2.5 User documentation

System will be "self-documenting" in a way that it will not require any extra knowledge to use it. The goal is to make the UI self explanatory.

##### 2.6 Assumptions and dependencies

Assumptions
- Website must run flawlessly on deployment
- Easy to use for users
- Users may access the page from computer or mobile devices
- 

Dependencies
- JAMK's login system is assumed to be embedded on the site for login.
- Information of items and users will be stored on a database

#### 3 System features

##### 3.1 Functional requirements

###### 3.1.1 Functional requirement 1

Title: Make a loan
Desc: User can make a new loan on a book that is available for loaning. If not, user can not make the loan. In the case item is in loan already, reference the user to FR 3.

###### 3.1.2 Functional requirement 2

Title: Make a reservation
Desc: If book is already loaned, user can make reservation for a loan to start after the last loan period has ended.

###### 3.1.3 Functional requirement 3

Title: Extend loan time
Desc: If no reservation for the book is made, user can select to extend the loan time for one (1) more loan period at a time.

###### 3.1.4 Functional requirement 4

Title: Login
Desc: JAMK's log in system must be embedded on the site for users to use their existing credentials for login. No other way for login will be implemented.

##### 3.2 System requirements

Web page must run flawlessly on mobile devices and on computer. 

As the product will be a web page application, no additional application has to be developed for mobile devices. However, while opening the site on mobile devices, whether it is a Android or IOS device, it has to open on mobile view.

On computer, the site has to be usable on Chromium based web browsers as well as on Firefox.