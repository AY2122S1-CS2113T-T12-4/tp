#Developer Guide Draft

##Introduction
Restaurant Buddy is a command-line-interface (CLI) application for **restaurant managers** to 
help **keep track of restaurant data** such as its employees, dishes and ingredients in storage.

##Contents
* Architecture
  * Employee Component
  * Ingredient Component
  * Dish Component
  * Storage Component

* Design and Implementation
* Appendix
  * Product Scope
  * User Stories
  * Non Functional Requirements
  * Glossary
  * Instructions for Manual Testing



##Architecture
The Main component has 2 classes, MainParser and MainUI. It is responsible for parsing user commands and 
displaying messages to interact with the user.

The rest of the app consists of 4 components:  

1. Employee: Modify data related to employee classes  

2. Ingredient: Modify data related to ingredient classes  

3. Dish: Modify data related to dish classes  

4. Storage: Reads and writes data to and from the hard disk  

###Employee Component
The employee component consists of the following four classes: *Employee*, *EmployeeList*, *EmployeeParser* 
and *EmployeeUI*.

* *Employee* stores the name and phone number of an individual employee working at the restaurant, as well as methods 
to retrieve employee information.

* *EmployeeList* is an array list of Employees.

* *EmployeeParser* contains operations that decode user inputs into meaningful commands, and modifies the list of 
employees accordingly.

* *EmployeeUI* contains methods that display messages that interacts with the user.

###Ingredient Component
The ingredient component consists of the *Ingredient*, *IngredientList*, *IngredientParser*, and *IngredientUI* classes.  

* *Ingredient* stores the name and quantity of a particular ingredient used by the restaurant, as well as methods to 
retrieve ingredient data.  

* *IngredientList* is an array list of Ingredient.  

* *IngredientParser* contains operations that decode user inputs into meaningful commands, and modifies the list of 
ingredients accordingly.  

* *IngredientUI* contains methods that display messages to interact with the user.  

###Dish Component
The dish component consists of the *Dish*, *Menu*, *DishParser*, and *DishUI* classes.  

* *Dish* stores the name, price and discount of a certain dish sold by the restaurant and the methods used to retrieve 
them.

* *Menu* is an arrayList of Dish.

* *DishParser* contains methods that decode user inputs into meaningful parameters and modify the menu accordingly.  

* *DishUI* contains methods that display messages to interact with the user.  

###Storage Component
The storage component has a *Storage* class which can load data from the file and save data into the file with the 
methods to encode and decode data.  

##Design and Implementation  

###Add Employee Feature
The mechanism of adding an employee into the list of employees is facilitated by *EmployeeParser*. It first creates a 
new instance of *Employee*, and adds it to the existing instance of *EmployeeList*. A confirmation message is then 
displayed to the user.

###List Employees Feature
The mechanism for listing all current employees in the list of employees is facilitated by *EmployeeParser*. It checks 
if the current instance of *EmployeeList* is empty, and if it is, displays a message to inform the user that the 
employee list is empty. Otherwise, it displays all employees and their information in the list to the user.

###Remove Employee Feature
The mechanism of removing an employee from the employee list is facilitated by *EmployeeParser*. It identifies the 
index of the employee to be removed from the current instance of *EmployeeList*, and removes that instance of 
*Employee* from the list. It then displays a message to the user to inform them of the successful deletion.

###Add Ingredient Feature
The mechanism of adding an ingredient into the ingredient list is facilitated by *IngredientParser*. It creates a new 
instance of Ingredient, and adds it to the existing instance of IngredientList. It then calls a method from 
*IngredientUI* to display a confirmation message to the user.

###List Ingredients Feature
The mechanism for listing all existing ingredients in the ingredient list is facilitated by *IngredientParser*. It 
checks if the existing instance of *IngredientList* is empty or not, and calls a method from *IngredientUI* to 
display the entire list of ingredients and their quantities to the user.

###Remove Ingredient Feature
The mechanism of removing an ingredient from the ingredient list is facilitated by *IngredientParser*. It identifies 
the index of the ingredient to be removed from the existing instance of *IngredientList* and removes that instance of 
Ingredient from the list. It then calls a method from *IngredientUI* which displays to the user that the deletion was 
successful.

###Add Dish Feature
The mechanism of adding a dish into the menu is facilitated by *DishParser*. It creates a new instance of 
Dish, and adds it to the existing instance of *Menu*. It then calls a method from DishUI to display a confirmation 
message to the user.

###List Menu Feature
The mechanism for listing all existing dishes in the menu is facilitated by *DishParser*. It checks if the 
existing instance of *Menu* is empty or not, and calls a method from *DishUI* to display the entire menu, 
together with the corresponding prices of each dish, to the user.

###Remove Dish Feature
The mechanism of removing a dish from the menu is facilitated by *DishParser*. It identifies the index of the 
dish to be removed from the existing instance of *Menu* and removes that instance of the dish from the menu. 
It then calls a method from *DishUI* which displays to the user that the deletion was successful.

###Save Storage Feature
The mechanism of saving the data into the file is facilitated by *Storage*. After executing the bye command, the 
program goes into saving date stage automatically. It opens the file with a file writer, and for every list the program 
has, it gets the item from them. Then, it encodes the string representation of the item, and writes it into the file.   

Besides, the three lists are stored in sequence as below,

###Load Storage Feature
The mechanism of loading the data from the file is facilitated by *Storage*. It opens the file with a file reader and 
if there are no files to open, it will automatically create a new file of default address. Every line read from the 
file would be decoded with methods to create a new *Employee*/*Dish*/*Ingredient* item, and add it into the list which 
is generated.  

Besides, the three types of new item are identified before decoding it, and the decoding methods are worked on at the 
same time.

##Appendix

###Product Scope

###User Stories

###Non Functional Requirements

###Glossary

###Instructions for Manual Testing

