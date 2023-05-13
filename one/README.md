# The AirBnB Clone Project


## Project Description
In the initial phase of the AirBnB clone project, our focus was on developing the backend and integrating it with a console application using the Python cmd module.

Data (python objects) generated are stored in a json file and can be accessed with the help of the json module in python

## Description of the command interpreter:
The command line interpreter acts as the front of the web application, providing a platform for users to engage with the backend,  which has been developed using

Python's object-oriented programming (OOP) principles.By utilizing the command line interpreter, users can interact with the backend and perform various actions.

These actions include creating new objects, such as a new User or a new Place, retrieving objects from different data sources like files or databases

performing operations on objects such as counting or computing statistics, updating attributes of objects, and destroying objects.

To facilitate these functionalities, the command line interpreter is integrated with a file storage system where the data, represented as Python objects, 

is generated and stored in a JSON file. The Python json module simplifies the process of accessing this data, enabling easy retrieval and manipulation

## How to start it
These instructions will get you a copy of the project up and running on your local machine (Linux distro) for development and testing purposes.

## Installing

To obtain the simple shell program and its dependencies, it is necessary for you to clone the project's repository on Github

```
https://github.com/kingbascee/AirBnB_clone.git
```
Upon successfully cloning the repository, you will discover a folder named "AirBnB_clone." Inside this folder, you will find multiple files essential for 
the program's functionality.

Here are the descriptions of the mentioned files in the repository:

- `/console.py`: This serves as the main executable for the project and functions as the command interpreter.

- `models/engine/file_storage.py`: This file contains a class responsible for serializing instances to a JSON file and deserializing JSON files back to instances.

- `models/__init__.py`: Within this file, you will find a unique `FileStorage` instance specifically designed for the application.

- `models/base_model.py`: This file defines a class that encompasses common attributes and methods shared by other classes.

- `models/user.py`: The `User` class inherits from the `BaseModel` class, and it is implemented within this file.

- `models/state.py`: The `State` class, which inherits from `BaseModel`, is implemented in this file.

- `models/city.py`: Inside this file, you will find the `City` class, which also inherits from `BaseModel`.

- `models/amenity.py`: The `Amenity` class, inheriting from `BaseModel`, is defined in this file.

- `models/place.py`: This file contains the `Place` class, which inherits from `BaseModel`.

- `models/review.py`: Inside this file, you will find the `Review` class, which also inherits from `BaseModel`.



## How to use it
The program operates in two distinct modes: Interactive and Non-interactive.

In Interactive mode, the console presents a prompt (hbnb) that indicates the user can input and execute commands. 

After running a command, the prompt reappears, awaiting a new command. 

This process can continue indefinitely unless the user chooses to exit the program.

In **Interactive mode**, the console will display a prompt (hbnb) indicating that the user can write and execute a command. 

After the command is run, the prompt will appear again a wait for a new command. This can go indefinitely as long as the user does not exit the program.

```
$ ./console.py
(hbnb) help

Documented commands (type help <topic>):
========================================
EOF  help  quit

(hbnb) 
(hbnb) 
(hbnb) quit
$
```

In **Non-interactive mode**, the shell will need to be run with a command input piped into its execution so that the command is run as soon as the Shell starts. In this mode no prompt will appear, and no further input will be expected from the user.


```
$ echo "help" | ./console.py
(hbnb)

Documented commands (type help <topic>):
========================================
EOF  help  quit
(hbnb) 
$
$ cat test_help
help
$
$ cat test_help | ./console.py
(hbnb)

Documented commands (type help <topic>):
========================================
EOF  help  quit
(hbnb) 
$
```

## Format of Command Input

In order to give commands to the console, these will need to be piped through an echo in case of  **Non-interactive mode**.

In  **Interactive Mode**  the commands will need to be written with a keyboard when the prompt appears and will be recognized when an enter key is pressed (new line). As soon as this happens, the console will attempt to execute the command through several means or will show an error message if the command didn't run successfully. In this mode, the console can be exited using the **CTRL + D** combination,  **CTRL + C**, or the command **quit** or **EOF**.

## Arguments

Most commands have several options or arguments that can be used when executing the program. In order for the Shell to recognize those parameters, the user must separate everything with spaces.

Example:

```

user@ubuntu:~/AirBnB$ ./console.py
(hbnb) create BaseModel
49faff9a-6318-451f-87b6-910505c55907
user@ubuntu:~/AirBnB$ ./console.py

```

or

```
user@ubuntu:~/AirBnB$ ./console.py $ echo "create BaseModel" | ./console.py
(hbnb)
e37ebcd3-f8e1-4c1f-8095-7a019070b1fa
(hbnb)
user@ubuntu:~/AirBnB$ ./console.py
```

## Available commands and what they do

The recognizable commands by the interpreter are the following:
|Command| Description |
|--|--|
| **quit or EOF** | Terminates the program. |
| **Usage** | Enter the command alone. |
| **-----** | **-----** |
| **help** | Provides a description of how to use a specific command. |
| **Usage** | Enter the command alone, or use **help <command>** to get information on a particular command. |
| **-----** | **-----** |
| **create** | Generates a new instance of a valid `Class`, saves it to the JSON file, and prints the `id` of the created instance. Valid classes include BaseModel, User, State, City, Amenity, Place, and Review. |
| **Usage** | **create <class name>** |
| **-----** | **-----** |
| **show** | Displays the string representation of an instance based on the class name and `id`. |
| **Usage** | **show <class name> <id>** --or-- **<class name>.show(<id>)** |
| **-----** | **-----** |
| **destroy** | Deletes an instance based on the class name and `id`, and saves the changes to the JSON file. |
| **Usage** | **destroy <class name> <id>** --or-- **<class name>.destroy(<id>)** |
| **-----** | **-----** |
| **all** | Prints the string representation of all instances, whether based on a specific class name or not. |
| **Usage** | Enter the command alone, or use **all <class name>** to display instances of a specific class. --or-- **<class name>.all()** |
| **-----** | **-----** |
| **update** | Updates an instance by modifying or adding attributes based on the class name and `id`, and saves the changes to the JSON file. |
| **Usage** | **update <class name> <id> <attribute name> "<attribute value>"** --or-- **<class name>.update(<id>, <attribute name>, <attribute value>)** --or-- **<class name>.update(<id>, <dictionary representation>)** |
| **-----** | **-----** |
| **count** | Retrieves the number of instances of a specific class. |
| **Usage** | **<class name>.count()** |

## Authors

Ayodeji Ariyo <isaacayodejiariyo@gmail.com>

Bassey <bascee@gmail.com>