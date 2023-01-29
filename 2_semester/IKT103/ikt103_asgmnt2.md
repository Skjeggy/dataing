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
less (<than)
suitability
3 years old ?

## 1.2
The HomeBrew Coffee machine makes up to 10 cups of coffee at a time. The user places a filter in the filter holder, fills the filter with coffee grounds, and slides the filter holder into its receptacle. The user then pours up to 10 cups of water into the water strainer and presses the "Brew" button. The water is heated until boiling. The pressure of the evolving steam forces the water to be sprayed over the coffee grounds, and coffee drips through the filter into the pot. The pot is kept warm for extended periods by a warmer plate, which only turns on if there is coffee in the pot. If the pot is removed from the warmer plate while coffee is sprayed over the grounds, the flow of water is stopped, so that brewed coffee does not spill on the warmer plate. The following hardware needs to be monitored or controlled.

-   The heating element for the boiler. It can be turned on or off.
-   The heating element for the warmer plate. It can be turned on or off.
-   The sensor for the warmer plate. It has three states: warmerEmpty, potEmpty, and potNotEmpty.
-   A sensor for the boiler, which determines if there is water present or not. It has two states: boilerEmpty or boilerNotEmtpy.
-   The brew button. This momentary button starts the brewing cycle. It has an indicator that lights up when the brewing cycle is over and the coffee is ready.
-   A pressure-relief valve that opens to reduce the pressure in the boiler. The drop in pressure stops the flow of water to the filter. It can be opened or closed.

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