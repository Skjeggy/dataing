---
alias: Assignment 2 - OOA
---

# 1. OOA
Use [[OOA|object oriented analysis]].

## 1.1
The customer enters the store to buy a toy. It has to be a toy that his daughter likes and it must cost less than 50 Euro. He tries a videogame, which uses a data glove and a head-mounted display. He likes it.

An assistant helps him. The suitability of the game depends on the age of the child. His daughter is only 3 years old. The assistant recommends another type of toy, namely a boardgame. The customer buy the game and leaves the store.

### nouns
Customer (class)
	Child (class)
		Age (attribute)
Store (class)
Toy (class)
	Game (subclass)
		Board game 
		Video game 
			Data glove and head-mounted display
	
	Euro - attribute
Assistant (class)

### adjectives
likes
less (<than)
likes
suitability
3 years old ?

## 1.2

# 2. UML

## 2.1 Class diagram
You are tasked with designing a software system for banks. Sounds familiar? Design the classes using UML. This solution must include inheritance in some way.

The bank system should keep track of the following information:

-   Accounts
-   Credit cards
-   Customers
-   Employees

Use your existing knowledge of banks to model the classes for this system. Generalize common information in base classes and derive from them.

You can use this tool:  
[https://www.planttext.com/Links to an external site.](https://www.planttext.com/)

With these settings to get the same look as in the lectures:

```
@startuml  
!theme plain  

skinparam classAttributeIconSize 0  
hide circle
```

## 2.2 Discussion

Was inheritance the right choice for this system? Why / why not? What are the advantages and disadvantages of inheritance?

Length: 200 words.