Task 2 


First, take a look at the following requirements for the new system. Your project manager passed them along with the data model ticket:

The system will help manage multiple financial advisors’ clients.
Financial advisors must be able to create, update, and remove clients.
Each financial advisor can have numerous clients.
Financial advisors will be using the system during standard business hours from 9 to 5 on weekdays.
Each client will have a portfolio.
Client portfolios may contain zero or more securities.
Financial advisors must be able to create, update, and remove securities from client portfolios.
Every security has a name, a category, a purchase date, a purchase price, and a quantity.
The system must have 99% uptime.
The system must expose a React dashboard.
The system’s backend must use the Spring framework for Java.
The system must store data in a relational database.
The system must be highly scalable.

Here is the background information on your task
You’ve ironed out the data model for the new system and just received approval for it from your project manager. Time to move on to the next step and actually write some code!

Your team has decided to manage the system’s data using the Java Persistence API, or JPA for short. The JPA is an object-relational mapping tool (ORM tool) - a means to bridge the gap between Java objects and data held in a relational database. The idea is that each Java object registered with the JPA has a representation of its state persisted to an external database. As you modify the Java object, the corresponding data object is updated as well. As such, when an application closes, all of its data is already saved to the database. The JPA lets us reason about transactions using java objects rather than raw data, and handles the conversion for us behind the scenes.

Fortunately, Spring comes with thorough support for the JPA, and actually allows for multiple database backends. Setting up a project to use Spring with the JPA is relatively straightforward, but you don’t have to worry about it. Someone on your team has already put together a project scaffold for the system backend, so you can focus on implementing your data model rather than drowning in a sea of Java boilerplate!

Here is your task
Your task is to implement the data model you created in the previous task within the provided Spring application. Follow these steps carefully:

Fork and clone the starter repo, which can be found here. If you are unfamiliar with Git, read through the first two chapters of the Git book, found here. Git is one of a developer’s most frequently used technologies, so it’s worth taking some time to get acquainted with it.
Download and install IntelliJ if you haven’t already. IntelliJ is one of the best Java IDEs on the market and can be found here.
Open up the project in IntelliJ, then take some time to explore the codebase. Get a feel for what each class is doing. It’s okay if you don’t understand how part of the code works; there are lots of gotchas in Spring development. The goal is to become familiar with the overall flow of the program.
Time to get to work! Create a class for each entity in your data model (these should be placed in the entities directory). Respect the following when implementing your data model:
Each entity must be annotated with the @Entity type, which can be found in the javax.persistence package.
Each id must be auto-generated.
Each instance variable must contain either a column or a relationship annotation.
Each class must contain a constructor which initializes all instance variables.
Each class must expose a getter and setter for each instance variable (no setter for the id field is required).
Lean on the existing entities (one has been provided for you) for hints on how to accomplish the above.
When you are finished implementing your data model, commit and push your changes to GitHub. Then, submit a link to your project repo in the next step. Good luck!
