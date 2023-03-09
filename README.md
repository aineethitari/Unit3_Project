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

### Overall Development of the Project
In the development of this project, there are 2 main parts which are the Graphical User Interface through KivyMD; the functions, which are developed using Python programming language; and the database, which is processed with SQLite3.

### Using KivyMD for the Graphical User Interface (GUI)
For the development of the GUI, KivyMD Library which contains material design widgets to organize the aesthetics of the interface. In this project there are many classes from the kivymd library that are imported to develop the components of the application: MDApp, MDScreen, MDDatatable and MDDialog. There are two parts in the development of the GUI, the first part is developed in the Python file, and the second part is developed in the kivy file. The python file may also contain other methods that are used for the functionality of the application as well. 

### Setting up Python file

```.py
from kivymd.app import MDApp #app builder
from kivymd.uix.datatables import MDDataTable #table in the app
from kivymd.uix.screen import MDScreen #different screens in the app
from kivymd.uix.dialog import MDDialog #pop up screen
from secure_password import encypt_password, check_password #hash password
import sqlite3 #connect to database

```
**Figure 9** The code starts with setting up the libraries and classes that are used to develop this program. To create the application, the program needs an app builder which is the “MDApp” application class from the kivymd library. From the kivymd library, MDDataTable, which is used to create the table shown in the application is also imported, MDScreen is used to create different screens in the application, MDDialog is used to show a pop up screen, secure password is a library that I created for password encryption, and sqlite3 is imported to process the database.

### Building the App with MDApp

```.py
class example_login(MDApp): #app builder
   def build(self):
       return
```
**Figure 10** This is the class for building the application which is inherited from the MDApp class from the kivymd library. The class name is the name of the kivy file “example_login”. The class includes a method called “build” which is used to build the application and connect the python file to the kivy file.

### Setting up the Screens with MDScreen

<img width="308" alt="screens" src="https://user-images.githubusercontent.com/112055062/223947719-52c6fd0b-bdd2-4a2d-ac67-a30bf5d5aed6.png">

**Figure 11** The screens in the application are developed by classes inheriting from the MDScreen class from the kivymd library. Each screen has its own class in the python file. The main screens in this application are WelcomeScreen, LoginScreen, RegistrationScreen, HomeScreen, NewItemScreen, and ClosetScreen.

### Visual Data Table in the Application

```.py
class ClosetScreen(MDScreen):
   data_table = None

   def on_pre_enter(self, *args): #create table
       # b4 the screen is created the code is run
       self.data_table = MDDataTable(
           size_hint=(.8, .5),
           pos_hint={"center_x": .5, "center_y": .5},
           use_pagination=True,
           check=True,
           # title of the columns
           column_data=[("id", 40),
                        ("user_id", 30),
                        ("item", 40),
                        ("category", 30),
                        ("color", 30),
                        ("location",40),
                        ("brand",40),
                        ]
       ) #info of the table
       self.data_table.bind(on_row_press=self.row_pressed)  # check the row method name change so its more easy to understand,
       self.data_table.bind(on_check_press=self.check_pressed) #check the check
       self.add_widget(self.data_table)  # add table to the GUI
       self.update() #update table
```
**Figure 12** The data table in this application is shown in the Seek Closet Screen which is in the class ClosetScreen inherited from the MDScreen class. The table in this class is created using a method called “on_pre_enter”, which creates the table showing the items in the closet. The settings of the table are added which are, for example, the size of the table, setting for page options, check marks, and information of the columns (id, user_id, category, color, location, and brand). This table fulfills success criteria number 4 where the application shows the brand of the item, the color, and the location of the item.

### Pop up screens using MDDialog
```.py
if item=="" or category=="" or color=="" or location=="" or brand =="": #if the fields are blank
   dialog = MDDialog(title="Not enough information",
                     text=f"Please fill in information") #pop up screen
   dialog.open() #show dialog
```
**Figure 13** MDDialog is used to show a pop up screen which can have messages for the user. In the application, these pop up screens are used as a confirmation when the user entered information in text fields such as the item information form, and confirmation for inserting item to the database. Figure 13 shows the use of MDDialog when one of the fields for the information of the item is not filled. A pop up screen will show up saying not enough information and asking the user to refill the information. 

### Kivy File

Apart from the python file, to develop the user interface, we also need a Kivy file which is written in the kivy language. The file is organized in layers with different elements. The file starts with listing the application screens and its layers.

```.py
ScreenManager:


   WelcomeScreen:
       name: "WelcomeScreen"

   LoginScreen:
       name: "LoginScreen"

   RegistrationScreen:
       name: "RegistrationScreen"

   HomeScreen:
       name: "HomeScreen"

   ClosetScreen:
       name: "ClosetScreen"

   NewItemScreen:
       name: "NewItemScreen"
```
**Figure 14** shows the screens in the application which is organized in layers. Therefore, the first screen that will show in the application when the user enters the application is the “WelcomeScreen”. The other screens could be accessed by the functions that are added to the application.

### Background and boxes with FitImage and MDCard
As the last success criteria says that the application has a simple interface, the program is organized with backgrounds and layers. The aesthetics of the program comes from the background which is a picture of a gradient graphic design. This image was added with the technique called FitImage which allows the user to add a picture file. In figure 15, the image file name is called “bg.jpeg”. However, to make a simple interface, the user needs to be able to read the information on the application clearly, so we use MDCard as a white base background. MDCard is a box with round edges used to contain content, which in this case, an MDLabel text is within the card.

```.py
<WelcomeScreen>:
   FitImage:
       source: "bg.jpeg"

   MDCard:
       size_hint: .6,.8
       pos_hint: {"center_x":.5, "center_y":.5}
       orientation: "vertical"
       spacing: dp(10)
       padding: dp(10)


       MDLabel:
           font_style: "H3"
           text: "Welcome to Zelan's Zazzy Closet"
           halign: "center"
```
**Figure 15** shows the welcome screen which has an image as a background, a card on top, and text saying “Welcome to Zelan’s Zazzy Closet” within the card.

### MDLabel
As the name says, MDLabel is the text function of the kivy language where the developer can adjust the size of the text, the style of the text, the message of the text, and its alignment.
```.py
MDLabel:
   size_hint: 1,.05
   font_style: "H2"
   text: "Registration"
   halign: "center"
```
**Figure16** The MDLabel widget has the settings of a size of taking up full space in the horizontal side, and 0.05 in the vertical side. The font style “H2” means header style 2, the text message is Registration and the horizontal alignment is placed at the center.

### MDRaisedButton
To operate the application, I have used buttons to allow users to click on and navigate them to certain actions such as going to another page, or submitting information.

```.py
MDRaisedButton:
   size_hint: .4,.2
   pos_hint: {"center_x":.5, "center_y":.5}
   text: "Explore Closet"
   md_bg_color: "C893E8"
   on_press: root.parent.current = "LoginScreen"
```
**Figure 17** According to the figure, MDRaisedButton is used to change the screen when it is pressed. The settings of the button says that the size takes up 0.4 of the horizontal, and 0.2 of the vertical. The position is at the middle as it is .5 of center x and y. There is a text on the button saying “Explore Closet”. The color of the button is the hex color code “C903E8”. When the user presses the button, the screen will change to the LoginScreen.

### Input through MDTextField
In the application, users may need to input information to the program such as username, password, or information of the items. MDTextField widget is used as a field to receive texts from the users. 

```.py
MDTextField:
   id: email
   hint_text: "enter email"
   icon_left: "email"
   pos_hint: {"center_x":.5}
   size_hint: .8, .1
   helper_text_mode: "on_error"
   helper_text: "Please enter an actual email"
```
**Figure 18** shows the text field for entering email in the registration screen.  The id of the widget is called “email”. The field will also have a text on it to inform the user on what to input by using “hint_text” as it says “enter username”. There is an email icon next to the text field by using icon_left.  The position and the size can also be adjusted with “pos_hint” and “size_hint”. When there is an error in from the user’s input, the program will also show an error message saying “Please enter an actual email” through “helper_text’.

### Organizing the pages with MDBoxLayout
To make the interface organized, I used an organizing tool called “MDBoxLayout” which is an invisible box that can contain widgets within it. The widgets will be organized based within the MDBoxLayout. 
```.py
MDBoxLayout:
   size_hint: 1,.1
   spacing: dp(10)
   padding: dp(10)

   MDRaisedButton:
       id: login
       text: "Back"
       md_bg_color: "#93D3E8" #blue
       on_press: root.parent.current = "LoginScreen"
       size_hint: .5,1


   MDRaisedButton:
       text: "Signup"
       md_bg_color: "#E893B1" #pink
       on_press: root.try_register()
       size_hint: .5,1

```
**Figure 19** shows the code for a Box Layout that has an organizing adjustment of spacing and padding with 10 density pixels. The box contains 2 widgets which are both buttons (MDRaisedButton). The two buttons will have the spacing and padding based on the settings underneath the MDBoxLayout.

### Checkbox using MDCheckbox
According to success criteria #3 “The application provides a visual function to see items being classified in categories: jewelry, top, bottom, shoes”. I used checkboxes to limit the user’s input in categories of the item by allowing them to choose between the 4 categories with checkboxes. 

```.py
MDBoxLayout:
   MDCheckbox:
       id: tops
       group: 'group1' #this group is so that all the checkboxes are linked and only one can be selected
       size_hint: None, None
       size: dp(48), dp(48)
       active: True
       on_active: root.checkbox_click(self, self.active, "Tops")
       pos_hint: {"center_y":.5}
   MDLabel:
       text: 'Tops'
       pos_hint: {"center_y":.5}
       font_size:30

MDBoxLayout:
   MDCheckbox:
       id: bottoms
       group: 'group1'
       size_hint: None, None
       size: dp(48), dp(48)
       on_active: root.checkbox_click(self, self.active, "Bottoms")
       pos_hint: {"center_y":.5}
   MDLabel:
       text: 'Bottoms'
       font_size:25
       pos_hint: {"center_y":.5}

MDBoxLayout:
   MDCheckbox:
       id: shoes
       group: 'group1'
       size_hint: None, None
       size: dp(48), dp(48)
       on_active: root.checkbox_click(self, self.active, "Shoes")
       pos_hint: {"center_y":.5}
   MDLabel:
       text: 'Shoes'
       pos_hint: {"center_y":.5}

MDBoxLayout:
   MDCheckbox:
       id: jewelry
       group: 'group1'
       size_hint: None, None
       size: dp(48), dp(48)
       on_active: root.checkbox_click(self, self.active, "Jewelry")
       pos_hint: {"center_y":.5}
   MDLabel:
       text: 'Jewelry'
       pos_hint: {"center_y":.5}
       font_size:25
```
**Figure 20** shows the code in kivy language of the 4 checkboxes that are created to allow the users to choose the category of the item. Each checkboxes has its own id to connect with the Python file. They all fit in the same group, “group1”, so all the checkboxes are linked and only one can be selected. The “on_active” allows the checkbox to be clicked and the information will be sent to the Python code as a string.

## Developing the functions through Python 

### Registration System
This is the method for registering new email and passwords to fulfill success criteria #1 where the client wants an application that has a login system that uses a hash password or a pin number. Therefore, I have created a registration system which allows the user to create a new account. 

```.py
def try_register(self): #registration method
   user = self.ids.username.text #user text field
   email = self.ids.email.text #email text field
   password = self.ids.password.text #password text field
   password_check = self.ids.password_check.text #password confirmation text field
   if "@" not in email: #checks that there's an @ in the email so it is an actual email
       self.ids.email.error = True #show error
   if password != password_check or len(password) < 7: # password entered does not match and have less than 7 characters
       self.ids.password_check.error = True #show error
       self.ids.password.error = True
       self.ids.password_check.md_bg_color = "red"
   else:  # password match
       db = database_worker("login_database.db") #connect to the database
       hash = encypt_password(password) #turn password to hash
       query = f"INSERT into users (email, password, username) values('{email}','{hash}','{user}')" # insert info into the table users
       db.run_save(query)
       db.close()
       print("Registration completed")
       self.parent.current = "LoginScreen" #change to login screen
```

**Figure 21** shows the Python code of the registration method where the users are asked to input a new username, email, password, and a password confirmation.

### Email Policy

```.py
if "@" not in email: #checks that there's an @ in the email so it is an actual email
   self.ids.email.error = True #show error
```

**Figure 22** There is a validation system for email to make sure that the user input an actual email address by requiring “@” to be in the input. If the “@” sign is not in the email input, the program will return an error message. 

### Password Policy
```.py
if password != password_check or len(password) < 7: # password entered does not match and have less than 7 characters
   self.ids.password_check.error = True #show error
   self.ids.password.error = True
   self.ids.password_check.md_bg_color = "red"
```
**Figure 23** There is a password policy that the user needs to enter a password that has at least 7 characters and the passwords input in the “password” textfield and the “password_check” textfield need to match to make sure that the user input the right password. This is done so by using an if statement where the passwords do not match and the characters does not reach 7 and the program will show an error message in the text field.

```.py
else:  # password match
   db = database_worker("login_database.db") #connect to the database
   hash = encypt_password(password) #turn password to hash
   query = f"INSERT into users (email, password, username) values('{email}','{hash}','{user}')" # insert info into the table users
   db.run_save(query)
   db.close()
   print("Registration completed")
   self.parent.current = "LoginScreen" #change to login screen
```
**Figure24** This shows what happens if the password entered passes the password policy. The program will connect to the database and transform the password into a hash with the function “encrypt_password” (see Figure 25). The user registration information is then inserted to the database through running the query, and the screen will be changed to the login screen.

### Hashing Password
According to success criteria #1, the client wants the password to be hashed. This is to ensure that the user is the only one who knows the password and that the developers would not be able to get the user’s password simply from looking at the database. We use a helper for hashing from a library called “passlib” which has a class called “CryptContext”.

```.py
from passlib.context import CryptContext #cyptographic algorithm
pwd_config = CryptContext(schemes = ["pbkdf2_sha256"],
                         default = "pbkdf2_sha256",
                         pbkdf2_sha256__default_rounds=30000
                         )
def encypt_password(user_password):
   #this function receives plain text password from the user and returns the hash salted
   return pwd_config.encrypt(user_password)

def check_password(user_password, hashed): #this is to check that the password entered is the same one as the hash
   return pwd_config.verify(user_password, hashed)
```

**Figure 25** is the python file called “secure_password” which imports a class “CryptContext” from the library “passlib”. It is a cryptographic algorithm which helps with hashing. There are two functions in this file: “encrypt_password” and “check_password”. The “encrypt_password” function receives the input password and converts it to a hash. The “check_password” function, on the other hand, receives the input password and the hashed password, then checks if the two match.

### Login System

After the account is created through the “try_register” method, the user can login to the application with their registered email and password. 
```.py
def try_login(self): #method to allow users to login
   email_entered = self.ids.email_in.text #email text field
   passwd_entered = self.ids.passwd_in.text #password text field
   db = database_worker(namedb="login_database.db") #connect to the database
   query = f"SELECT * from main.users where email = '{email_entered}'" #select in the database the email that matches
   result = db.search(query = query) #search the query
   db.close()
```
***Figure 26*** The figure above shows how the entered email is being searched in the database. The program receives the email and password input from the text field and saves it in the “email_entered” and “passwd_entered” variables. The program then runs a query which selects all from the “users” table in the database where the email matches the email entered.

```.py
if len(result)==1: # if the data matches
   id, email, hashed, uname = result[0] #means that id = result[0][0], email = result[0][1],...
   if check_password(hashed=hashed, user_password=passwd_entered):
       print("Login successful")
       self.parent.current = "HomeScreen" #change screen to homescreen
       HomeScreen.user_id = id #id of user that logged in
   else:
       self.ids.passwd_in.error = True #if the login is right but password is wrong show error
       print("Password don't match")
else:
   self.ids.email_in.error = True #show error
   self.ids.passwd_in.error = True
   print("Login incorrect")
```
**Figure 27** The figure shows the code when the email matches with the data in the database. It then checks if the password matches with the hash in the database through the “check_password” function. If both the email and the password matches, the screen will then change to the home screen. If the email does not match, the application will also show an email error. If the email is correct, but the password is not, it will also show an error message in the password field. The user will not be able to enter any other screens until both the email and the password matches.

### Save Item Method
In order to fulfill success criteria number 5 “the application allows the user to add and remove items”, I have created a method to receive input from the user through text fields and checkboxes and added them to the database. Moreover, the application also allows the user to add information of the item, the category, the color, the location, and the brand which fulfills success criteria 4.

```.py
def try_save_item(self): #method to save item
   item = self.ids.item.text #text field for item name
   category = self.selected_category #check box for category name
   color = self.ids.color.text #text field for color
   location = self.ids.location.text #text field for location
   brand = self.ids.brand.text #text field for brand

   if item=="" or category=="" or color=="" or location=="" or brand =="": #if the fields are blank
       dialog = MDDialog(title="Not enough information",
                         text=f"Please fill in information") #pop up screen
       dialog.open() #show dialog
   else:
       db = database_worker(namedb="login_database.db") #connect to databse
       query = f"INSERT into closet (user_id, item, category, color, location, brand) values ('{HomeScreen.user_id}','{item}','{category}','{color}','{location}','{brand}')"
       db.run_save(query) #run query to insert info of item
       db.close()
```
**Figure 28** shows the method where the information is received from the application saved in different variables as strings. There is an if statement to check that all the information is added. Then the information is saved to the “closet” table in the database.

### Delete Item Method
In order to fulfill success criteria 5, the application needs to be able to delete an item from the closet. I have created a function to delete the item from the database table.
```.py
def save(self): #delete row from table
   checked_rows = self.data_table.get_row_checks()
   print(checked_rows)
   # delete
   for r in checked_rows:
       id = r[0] #user id matches
       print(id)
       query = f"DELETE from closet where id={id}" #delete where id is the row that is checked
       print(query)
       db = database_worker("login_database.db")
       db.run_save(query)
   db.close()
   self.update()
```
**Figure 29** This is the method that deletes the checked row from the table. From this method, the program uses a for loop to get the user id of the row, and delete the row from the closet where id matches.

### Category Filter

According to success criteria 3, the client want the closet to be organized in categories. Therefore, I have created a method where a table only shows item data from the same category that is chosen.

```.py
def update(self, in_category="%"): #select all from the selected category
   # read database and update table
   db = database_worker("login_database.db")
   query = f"SELECT * from closet where category like '{in_category}' and user_id={HomeScreen.user_id}" #show table where the category is the selcted one and belongs to one user id
   data = db.search(query)
   db.close()
   self.data_table.update_row_data(None, data)  # data put in table
```
**Figure 30** The code shows that the query selects the items from the closet where the category matches the category that is selected. 

```.py
def showall(self): #show the entire closet table
   db = database_worker("login_database.db")
   query = f"SELECT * from closet where user_id={HomeScreen.user_id}" #all from closet table where user id is the one that is registered
   data = db.search(query)
   db.close()
   self.data_table.update_row_data(None, data) #put data in table
```
***Figure 31*** Apart from viewing the items through filtered categories, the users also have the option to view the items in full view. Every item that falls under the user’s account id will be shown in the table.

## Connect to Database
According to success criteria 2, the client wants information to be stored in a database. Therefore, a class called “database_worker” is used to set up the database through SQLite3.
```.py
class database_worker: #method to setup the database
   def __init__(self,namedb:str):
       self.connection = sqlite3.connect(namedb)
       self.cursor = self.connection.cursor()
```
**Figure 32** the class “database_worker” consists of methods where this is the initializer and two attributes are created which are “self.connection” and “self.cursor”. The connection attribute connects the database to the python file, and the cursor attribute establishes a cursor to the club members when they execute and run kivy files.

### Create Database Table

The database contains two data tables which is the “users” table and the “closet” table. The “users” table is used to store registration information and the “closet” table is used to store item information. 

```.py
def create_tables(self): #method to create the tables in the database
   query = f"""CREATE TABLE if not exists users(
       id INTEGER PRIMARY KEY,
       email text NOT NULL unique,
       password text NOT NULL,
       username text NOT NULL)""" #table for users table which stores user information

   query2=f"""           
           CREATE TABLE if not exists closet(
           id INTEGER PRIMARY KEY,
           user_id INTEGER,
           item text,
           category  text,
           color text,
           location text,
           brand text)""" #table for the closet which stores information of the items
   self.run_save(query) #run the query
   self.run_save(query2)
```
**Figure 33** To create a table, a query is run. The query would state the different columns in the two tables. When the program runs, it is in default to create a new table unless the table does not exist. 


# Criteria D-Functionality

# Citation
[1] “Passlib.context - Cryptcontext Hash Manager¶.” Passlib.context - CryptContext Hash Manager - Passlib v1.7.4 Documentation, https://passlib.readthedocs.io/en/stable/lib/passlib.context.html. 
[2] “Welcome to KIVYMD's Documentation!#.” KivyMD 1.1.1 Documentation, https://kivymd.readthedocs.io/en/1.1.1/. 
[3] “Philosophy¶.” Kivy, https://kivy.org/doc/stable/philosophy.html#:~:text=Kivy%20is%20flexible.,adapt%20to%20new%20technologies%20quickly. 

[4] S., Edward. “SQLite vs Mysql – What's the Difference.” Hostinger Tutorials, 21 Dec. 2022, https://www.hostinger.com/tutorials/sqlite-vs-mysql-whats-the-difference/#:~:text=Multiple%20Access%20and%20Scalability%20%E2%80%93%20SQLite%20vs%20MySQL,-SQLite%20does%20not&text=MySQL%20has%20a%20well%2Dconstructed,gets%20larger%20while%20using%20SQLite. 

[5] “Card#.” Card - KivyMD 1.1.1 Documentation, https://kivymd.readthedocs.io/en/1.1.1/components/card/index.html. 

[6] “Datatables.” DataTables - KivyMD 1.1.1 Documentation, https://kivymd.readthedocs.io/en/1.1.1/components/datatables/index.html. 

[7] “Screen.” Screen - KivyMD 1.1.1 Documentation, https://kivymd.readthedocs.io/en/1.1.1/components/screen/index.html. 

[8] “Dialog.” Dialog - KivyMD 1.1.1 Documentation, https://kivymd.readthedocs.io/en/1.1.1/components/dialog/index.html. 

[9] SQLite Documentation, https://www.sqlite.org/docs.html. 
