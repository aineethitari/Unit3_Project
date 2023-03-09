# Unit3_Project

![wardrobe](https://user-images.githubusercontent.com/112055062/223326409-ed67c022-db8c-4191-ad36-ec11d4573598.jpeg)

# Table of Content
1. [Criteria A](#criteria-a-planning)

2. [Criteria B](#criteria-b-solution-overview)

3. [Criteria C](#criteria-c-development)

4. [Criteria D](#criteria-d-functionality)

5. [Citation](#citation)

6. [Code](#code)

# Criteria A-Planning
## Problem Definition
My client has a large amount of clothing items, varying from different kinds of jewelries, tops, bottoms, to shoes. She often has trouble with how she can manage and keep track of where her clothing items go. After she stores one item in her wardrobe, they would disappear. One incident was when her father gave her jewelry that was passed on generations by generations, she lost the valuable family heirloom in her messy wardrobe. She felt extremely guilty and miserable that the tradition ended because of her. Since then, she decided to become a more organized person by using a tracker. She is in need of an application that will keep track of the items in her wardrobe that has the functions to let her add and remove items, organize by color, classify the items in categories, and is easy to go through.

## Success Criteria
1. The application has a login system that uses a password or a pin number
2. The application stores information in a database
3. The application provides a visual function to see items being classified in categories: jewelry, top, bottom, shoes
4. The application shows the brand of the item, the color, and the location of the item
5. The application allows the user to add and remove items
6. The application has a simple interface 

## Rationale for Proposed Solution
In this project, I will develop a closet tracker application that allows the client to view what is in their closet and put them in organized categories. The application will include a registration page and login page for each individual user. This is to make sure that different user’s clothing items do not get mixed up and so that no one can edit one user’s private information. The application will also include a home page which allows the user to choose the different functions of adding new items, or viewing their closet. The home page will be very simple because the client wants to be able to insert items and delete items quickly. If the user chooses the option of inserting items, they will be redirected to a new page which allows them to fill out the details of the new item: item name, category, location, brand. These details are the specific details that the client uses to picture what their clothes look like. For the seek closet page, the client will be able to view their items from a table which is the most organized way to look at the details of the items. They can also filter the table into categories if they are looking for a specific item. This is very useful for those who do not remember where their items are at. They can also delete the item if they have removed it from the previous location and it can be done very easily, using one delete button. The simplicity and functionality of this closet tracker is the most important part that the client wants. 

For the tools in this application, I will use KivyMD to develop the application interface, python 3.9 for the functions, and SQLite3 for the database. I am using KivyMD for the interface because KIvyMD is free to use which is good for a simple application that does not have a huge budget. It is also flexible to be used in many devices and  operating systems. It is also created to be used with the python programming language which is used in this project. [3]

 I have also chosen to use python 3.9 in this project because Python is a very powerful language that is simple and widely used. If there are further edits that need to be made, it is likely that other developers will be able to continue the project smoothly. There are also a large number of free libraries to use which makes it easy to create a GUI in this project.

Lastly, I have chosen to use sqlite3 for the database of this project because it is free which remains underneath the limited budget we have. It also does not need a server. To compare with MySQL, SQLite is suitable for small databases, which is what we need in this case. [4]

# Criteria B-Solution overview

## System Diagram of the Program

![IMG_7435](https://user-images.githubusercontent.com/112055062/223325525-a3d7705e-0299-4ebe-a2ee-2051bb63f52e.JPG)
**Figure1** This shows the system diagram of the program which consists of the input which is from the keyboard and the trackpad into the computer which is an Apple MacBook Pro 2020 with macOSMonerey 12.6. In the computer, the programming language that is used is Python 3.11 and a KivyMD library is used to develop the application. Python is connected to the SQLite database. Lastly the output, which is the app interface, is connected to the Python program.

## Wireframe Diagram of the GUI

![IMG_7437](https://user-images.githubusercontent.com/112055062/223385609-b9dac2d8-8039-4a95-9ccf-db119df72c8f.JPG)
**Figure2** This is the wireframe diagram for the GUI. The diagram shows the functions of each button on where it will direct the users to. The six screens in the applications are the welcome screen, login screen, registration screen, home screen, seek closet screen, and add item screen. As shown in the diagram above, the welcome screen is the first screen that the user will encounter when entering the application. There will be an “Explore Closet” button, which allows the user to proceed to the login screen. If the user does not have an account, they will have to start a new registration in the registration screen by clicking the “Registration” button. If they have an account they can enter their information and proceed to the home screen. In the registration screen, the user will be asked to fill in their information. Once they have filled out the blanks, they can press the “Signup” button. This button will take them back to the login screen before entering the Home screen. There are three main buttons in the home screen: seek closet, add item, and logout. The seek closet button will take the user to the Seek closet screen, which shows a table of the closet. The user can press the “Back” button to go back to the Home screen. In the Home screen, the “Add item” button takes the user to the “Add Item Screen”. This screen allows the user to fill in the information about new items to add into the closet. There is a “Back”  button which takes the user back to the Home screen. Lastly, in the home screen, the user can press the “Logout” button to head back to the login page. 

## ER Diagram of the Database 

![Blank diagram](https://user-images.githubusercontent.com/112055062/223399486-d1e9fed4-d347-4e78-8d26-1eeeceb73a98.jpeg)

**Figure 3** This is the ER Diagram for the database "login_database.db", which contains two tables: users and closet. The ER diagram above shows the relationship between these two tables that per one user there can be numerous closets. There are 4 columns in the users table: email, id (user id), password, and username. The information in these columns are collected from when the users login to the application. The closet table, on the other hand, is used to store the items that the users want to add to their closet. One user can enter as many items to the closet as they want. There are 7 columns in the table: id(item id), brand, location, user_id, item, color, and category.

## UML Diagram of the Program

![UML diagram](https://user-images.githubusercontent.com/112055062/223410991-fef4324b-ef87-4deb-bb2c-69b9f5c03c30.jpeg)

**Figure 4** This is the UML Diagram of the classes used in this project with the details of the attributes and the methods within each class. The classes are MDApp, database_worker, MDScreen, and other classes that inherit from the MDApp and the MDScreen class. The inheritance class from MDApp is the example_login(MDApp) class, which is the class that builds the application. The inheritance class from the MDScreen class are the screens in the program: WelcomeScreen(MDScreen), LoginScreen(MDScreen), RegistrationScreen(MDScreen), HomeScreen(MDScreen), NewItemScreen(MDScreen), ClosetScreen(MDScreen). Lastly, the class database_worker is used to set up the database with methods that involve creating the tables and editing them.

## Flow Diagram for the Registration Method

![Registration Flow Diagram](https://user-images.githubusercontent.com/112055062/223423319-d5db7b3e-5720-465b-a48b-dd7e3838d409.jpeg)

**Figure 5** The flow diagram above shows how the registration method works. According to the diagram, the programs get information of the user, email, password, and password confirmation from the user input in the application. Then it checks whether the email is an actual email address by checking if there “@” is in the email. If it is not an email, the program shows an error message for the email. Then the program checks whether the password entered and the confirmation password is the same and whether the password has more than 7 characters. If it does not fit the requirement, the program will show an error message. If the email and password entered fits the requirements, the program will connect to the database “login_database.db”, convert the entered password into a hash, and insert the hash, password, email, and user to the table “users”. The program will then proceed on to the next page which is the “LoginScreen”

## Flow Diagram for the Save Item Method

![save item flow diagram](https://user-images.githubusercontent.com/112055062/223440785-4960f3ba-f2dd-4871-813b-7e7c0c7478d5.jpeg)

**Figure 6** The flow diagram above shows how the method that saves an item to the closet works. The method starts with storing the user input of the item name, category, color, location, and brand into variables. Then if the input is an empty string, which means no input is added to the program, a pop up screen will show a message asking the user to fill in the information. If the information is filled out correctly, the program will connect to the database and insert the information entered by the user to the table “closet” and show a confirmation pop up screen. 

## Flow Diagram for Delete Item Method

![delete item method](https://user-images.githubusercontent.com/112055062/223451458-35ecb917-10e3-4c85-8872-c0558b0b9103.jpeg)

**Figure 6** The flow diagram shows how the delete method works. This method is used to delete items from the closet database table. The method includes storing the rows that are checked from the table in the application in a variable called “checks”. Then for every item in checks, the first item is then stored in a variable called “id”. The first item is the id of the item that is added to the closet. Then the program is connected to the database “login_database.db”. The program then deletes the row with the same id as the checked row from the database. The checked item will then be erased.

## Test Plan
|Description| Type| Inputs| Outputs|
|-----------------------|----------|----------------------------------------|-----------------------------------|
|Test the registration system| Unit test|1. Enter username, email, password, password check 2.Press the signup button|Information is successfully added to the database and the screen proceeds to the login page|
|Test the email validation in registration| Unit test| 1.Enter every blank field correctly, but enter a random string that is not an email in the email field 2.Press signup|The program returns an error in the email field|
| Test the password length validation| Unit test| 1.Enter every blank field correctly, but enter the same password with characters less than 7 in the two password fields. 2.Press signup| The program returns a red error message in the field|
| Test the password confirmation| Unit test| 1.Enter every blank field correctly, but enter different passwords in the two password field 2.Press signup| The program returns a red error message in the field|
| Test the login system|Unit test|1. Enter a registered email 2.Enter a registered password 3.Press Login button| The program proceeds to the next screen|
|Test the login system 2| Unit test|1.Enter a wrong email 2.Enter a password 3.Press login| The program shows error in the two text fields|
|Test the login system 3| Unit test| 1.Enter a correct registered email 2.Enter a wrong password 3.Press login| The program shows error only in the password field|
|Test the buttons and navigation in home screen| Integration Test| 1.Click the buttons in the application | After clicking the buttons, the page change to the correct page|
|Check the Table in the Seek Closet Page| Unit Test| 1.Scroll through the table in the table 2.Click to the 2nd page 3.Click on the category filters|The items in the table in the application matches the items in the table in the databese|
|Check the delete item system| Unit Test| 1.Click on a row 2.Click the delete button| The row is gone when the user refreshes the screen by reclicking the category filter button|
|Check the add item system| Unit test | 1.Fill out every field in the form 2.Press the insert button | The program returns a pop up screen confirming that the item inserted. The item is also added to the new screen|
|Check the add item system for error| Unit test| 1.Leave some fields blank 2.Press the insert button| The program returns a pop up screen asking the users to fill out the blanked fields.|
|Python code review| Code review| 1.Check if the code is easy for other developers to continue 2.Code has comments to explain each parts that need explanation 3.Variable names matches what the code does 3.There are no unnecessary lines| Code is commented clearly with organized structure. The code is easy to follow through.|

**Figure 7** Test plan of the program which consists of a description of the test, the type of the test(unit test, integration test, or code review), inputs for the test, and the expected outputs for the successful test. 

## Record of Tasks
| Task No | Planned Action| Planned Outcome| Time estimate | Target completion date | Criterion |
|-|--------|--------|---|---|---|
|1|Meet with the client|Discuss Problem definition| 5 min| 16 Feb 23| Criteria A|
|2|Meet with client| Finalize success criteria| 5 min | 16 Feb 23| Criteria A|
|3| Finish login system| Login system with password stored as a hash and nice simple visuals| 30 min| 26 Feb 23 |Criteria C|
|4| Create a Welcome Screen| Welcome Screen with nice visuals| 5 min| 26 Feb 23| Criteria C|
|5| Create a Home Screen| Homescreen with buttons that can go to other screens | 1 hr | 26 Feb 23 | Criteria C|
|6| Create a Add Item Screen| Screen with text boxes to add information| 3 hr|27 Feb 23| Criteria C|
|7| Connect add item screen to database| Screen can add information filled to the database | 1 hr |2 March 23| Criteria C|
|8| Create Seek closet screen| Screen with items that allow users to edit items in the closet and look at what is in the closet by categories| 3 hr| 2 March 23| Criteria C|
|9| Create the function of the seek closet screen |Function in python, so the user can see the items in the closet by category| 3 hr| 2 March 23| Criteria C|
|10| Show the client the prototype| Present in front of the client and take notes of the feedback| 10 min| 3 March 23| Criteria B|
|11| Write the rationale for proposed solution| Explanation of the reasons behind every decision made in developing this project| 1 hr| 7 March 23| Criteria B|
|12| Create citation section in the repository| citation for every links that is used| 20 min|7 March 2023| Criteria B| 
|13| Create System Diagram| System diagram that shows how the program works| 1 hr| 7 March | Criteria B|
|14| Write about the system diagram| Detailed explanation of the elements of the system and how the application functions| 15 min| 7 March| Criteria B|
|15| Create a wireframe diagram| Visual diagram that shows the different screens of the application and the buttons that directs it to each screen| 1 hr| 7 March| Criteria B|
|16| Write a description about the wireframe diagram| Explain to the client in detailed on how the diagram works, and guide them through every screen| 15 min| 7 March 2023| Criteria B|
|17| Create ER Diagram| Diagram that shows the relationship between the tables in the database| 30 min| 7 March| Criteria B|
|18| Write about the ER Diagram| Detailed description of the relationships in the diagram| 15 min| 7 March| Criteria B|
|19| Create UML Diagram| Diagram that shows the classes in the program, the attributes in it, and the methods| 30 min| 7 March| Criteria B|
|20| Write about UML Diagram| Detailed description of the UML Diagram| 15 min| 7 March| Criteria B|
|21| Create Flow Diagram for registration method| Flow diagram that is simple for the client to understand how the method works| 30 min| 7 March| Criteria B|
|22| Write about Flow Diagram for registration method| Detailed description of the flow diagram| 15 min| 7 March| Criteria B|
|23| Created the flow diagram for the adding new item method| The flow diagram shows how new item is added to the database through the application | 15 min| 7 March 23| Criteria B|
|24| Write about the flow diagram for adding new item| Detailed description of the flow diagram to establish a common understanding| 15 min| 7 March 23| Criteria B|
|25| Create flow diagram for delete item method| The flow diagram shows how the function for deleting item that is checked works| 30 min| 7 March 23| Criteria B|
|26| Write about the flow diagram for deleting item| Detailed description of how the flow diagram work so the client understands the method| 15 min| 7 March 23| Criteria B|
|27| Create the test plan table| test plan table with the following columns: description, type, inputs, and outputs| 5 min| 7 March 2023| Criteria B|
|28| Write the test plan| detail test plan | 15 min| 8 March 2023| Criteria B|
|29| Add comments to the code | Commented code with explanation to every confusing points| 30 min| 8 March 2023| Criteria B|
|30| Review whole code| Code has comments, appropriate variables,...| 20 min| 8 March 2023| Criteria B|
|31| List all techniques used| Techniques that are used to develop this application are listed clearly| 15 min| 9 March 2023| Criteria C|

**Figure 8** The table above is the record of task for the development of the project since the beginning to the very end which is the documentation process. The information in the table includes the number of the task, the planned action, the planned outcome, the time taken to complete the task, the date completed, and the criteria(Criteria A:Planning, Criteria B: Solution Overview, Criteria C: Development, and Criteria D: Functionality)

# Criteria C-Development

## List of techniques used
- Object-oriented programming (OOP)
- KivyMD Library
- Relational Databases
- SQLite, Object Relational Mapping
- Passlib Password Hashing Library
- If Statements
- For loops
- Variables

## Overall Development of the Project
In the development of this project, there are 2 main parts which are the Graphical User Interface through KivyMD; the functions, which are developed using Python programming language; and the database, which is processed with SQLite3.

## Using KivyMD for the Graphical User Interface (GUI)
For the development of the GUI, KivyMD Library which contains material design widgets to organize the aesthetics of the interface. In this project there are many classes from the kivymd library that are imported to develop the components of the application: MDApp, MDScreen, MDDatatable and MDDialog. There are two parts in the development of the GUI, the first part is developed in the Python file, and the second part is developed in the kivy file. The python file may also contain other methods that are used for the functionality of the application as well. 

**Setting up Python file**

```.py
from kivymd.app import MDApp #app builder
from kivymd.uix.datatables import MDDataTable #table in the app
from kivymd.uix.screen import MDScreen #different screens in the app
from kivymd.uix.dialog import MDDialog #pop up screen
from secure_password import encypt_password, check_password #hash password
import sqlite3 #connect to database

```
**Figure 9** The code starts with setting up the libraries and classes that are used to develop this program. To create the application, the program needs an app builder which is the “MDApp” application class from the kivymd library. From the kivymd library, MDDataTable, which is used to create the table shown in the application is also imported, MDScreen is used to create different screens in the application, MDDialog is used to show a pop up screen, secure password is a library that I created for password encryption, and sqlite3 is imported to process the database.

**Building the App**

```.py
class example_login(MDApp): #app builder
   def build(self):
       return
```
**Figure 10** This is the class for building the application which is inherited from the MDApp class from the kivymd library. The class name is the name of the kivy file “example_login”. The class includes a method called “build” which is used to build the application and connect the python file to the kivy file.

**Setting up the Screens**

<img width="308" alt="screens" src="https://user-images.githubusercontent.com/112055062/223947719-52c6fd0b-bdd2-4a2d-ac67-a30bf5d5aed6.png">

**Figure 11** The screens in the application are developed by classes inheriting from the MDScreen class from the kivymd library. Each screen has its own class in the python file. The main screens in this application are WelcomeScreen, LoginScreen, RegistrationScreen, HomeScreen, NewItemScreen, and ClosetScreen.



# Criteria D-Functionality
# Citation

[3] “Philosophy¶.” Kivy, https://kivy.org/doc/stable/philosophy.html#:~:text=Kivy%20is%20flexible.,adapt%20to%20new%20technologies%20quickly. 

[4] S., Edward. “SQLite vs Mysql – What's the Difference.” Hostinger Tutorials, 21 Dec. 2022, https://www.hostinger.com/tutorials/sqlite-vs-mysql-whats-the-difference/#:~:text=Multiple%20Access%20and%20Scalability%20%E2%80%93%20SQLite%20vs%20MySQL,-SQLite%20does%20not&text=MySQL%20has%20a%20well%2Dconstructed,gets%20larger%20while%20using%20SQLite. 
