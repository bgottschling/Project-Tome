#  Implementation Plan

## It would contain
- An Interface for character that contain getters and setters for Name, Age, Height, etc... 

- An Interfaces for character races to encapsulate racial traits into a portable template

- Multiple classes that implement the Character Interface and the Race Interface for the goal of creating the Character and Class(RPG) of the Character via a Class Factory. 

  **Note: This May be a lot of classes to define due to the possibilities of combinations. Is there a better way to instantiate a character object which abstracts the Class and Race into one object.**

- A Class Factory class would have 2 arguments, one for Race and one for Class to create a character object and a switch case statement would take the Race and the Class to determine the Race-Class combination and return a race-class object (character). 

  **Note: Same bottle-neck as above.**

## The Execution

- The Main class would take user input for the character's Race and the character's Class to call the Class Factory which returns a character object.
 - It might be worth creating a character abstract class that I can use to extend the unique class combination classes so it is easier to understand when handling the character objects. 

Like so:

    Character character = new ElfWizard();


- Then it would prompt the user for the characters Name which will be used to call a Setter method for the character.

- Prompts again for the size specifications(Tiny, Small, Medium, Large, Extra Large) which will also call a setter.

  **Note: Dependening on Race, size choices will be limited via some conditional flow.**

- Base attribute stats at 10 and gives stat points for allocation with a hard cap at 20 which call setters for each input provided.

  **Note: May be tricky to implement in a console application. It would be cool to find out how to do this.**

- Then calls the character object methods for abilities to test.

  **Note: Is there a better way than sticking everything in Main?** 

## Summary of Concerns

Would it be better to create a Character Creation class which will be instantiated in main to call a user creation method which prompts the user for input to create the character object and then prompts for inputs to set the character info?
 
Are there any current UI frameworks that I can use to prompt input instead of the Console? 

I have interest in transforming this into a API later to store values into a database. This is so that I can create a Web Application to work with these methods.



