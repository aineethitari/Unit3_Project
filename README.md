# Unit3_Project

![closet future](https://user-images.githubusercontent.com/112055062/223308489-a5827965-ff1a-422a-a6d6-d0ba33132330.png)
**fig.1** AI generated closet art [1]

# Table of Content
1. [Criteria A](#criteria-a-planning)

2. [Criteria B](#criteria-b-solution-overview)

3. [Criteria C](#criteria-c-development)

4. [Criteria D](#criteria-d-functionality)

5. [Citation](#citation)

6. [Code](#code)

# Criteria A-Planning
## Problem Definition
My client has a large amount of clothing items, varying from different kinds of jewelries, tops, bottoms, to shoes. She often has trouble with how she can manage and keep track of where her clothing items go. After she stores one item in her wardrobe, they would disappear. One incident was when her father gave her jewelry that was passed on generations by generations, she lost the valuable family heirloom in her messy wardrobe. She felt extremely guilty and miserable that the tradition ended because of her. Since then, she decided to become a more organized person by using a tracker. She is in need of an application that will keep track of the items in her wardrobe that has the functions to let her add and remove items, organize by color, classify the items in categories, and is easy to go through. [1]

## Rationale for Proposed Solution
In this project, I will develop a closet tracker application that allows the client to view what is in their closet and put them in organized categories. The application will include a registration page and login page for each individual user. This is to make sure that different user’s clothing items do not get mixed up and so that no one can edit one user’s private information. The application will also include a home page which allows the user to choose the different functions of adding new items, or viewing their closet. The home page will be very simple because the client wants to be able to insert items and delete items quickly. If the user chooses the option of inserting items, they will be redirected to a new page which allows them to fill out the details of the new item: item name, category, location, brand. These details are the specific details that the client uses to picture what their clothes look like. For the seek closet page, the client will be able to view their items from a table which is the most organized way to look at the details of the items. They can also filter the table into categories if they are looking for a specific item. This is very useful for those who do not remember where their items are at. They can also delete the item if they have removed it from the previous location and it can be done very easily, using one delete button. The simplicity and functionality of this closet tracker is the most important part that the client wants. 

For the tools in this application, I will use KivyMD to develop the application interface, python 3.9 for the functions, and SQLite3 for the database. I am using KivyMD for the interface because KIvyMD is free to use which is good for a simple application that does not have a huge budget. It is also flexible to be used in many devices and  operating systems. It is also created to be used with the python programming language which is used in this project. [3]

 I have also chosen to use python 3.9 in this project because Python is a very powerful language that is simple and widely used. If there are further edits that need to be made, it is likely that other developers will be able to continue the project smoothly. There are also a large number of free libraries to use which makes it easy to create a GUI in this project.

Lastly, I have chosen to use sqlite3 for the database of this project because it is free which remains underneath the limited budget we have. It also does not need a server. To compare with MySQL, SQLite is suitable for small databases, which is what we need in this case. [4]


## Success Criteria
1. The application has a login system that uses a password or a pin number
2. The application stores information in a database
3. The application provides a visual function to see items being classified in categories: jewelry, top, bottom, shoes
4. The application shows the brand of the item, the color, and the location of the item
5. The application allows the user to add and remove items
6. The application has a simple interface 

# Criteria B-Solution overview

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


# Criteria C-Development

# Criteria D-Functionality
# Citation

[1]“Ai Art Generator, AI Image Generator API.” Hotpot.ai, https://hotpot.ai/art-generator. 
[3] “Philosophy¶.” Kivy, https://kivy.org/doc/stable/philosophy.html#:~:text=Kivy%20is%20flexible.,adapt%20to%20new%20technologies%20quickly. 
[4] S., Edward. “SQLite vs Mysql – What's the Difference.” Hostinger Tutorials, 21 Dec. 2022, https://www.hostinger.com/tutorials/sqlite-vs-mysql-whats-the-difference/#:~:text=Multiple%20Access%20and%20Scalability%20%E2%80%93%20SQLite%20vs%20MySQL,-SQLite%20does%20not&text=MySQL%20has%20a%20well%2Dconstructed,gets%20larger%20while%20using%20SQLite. 
