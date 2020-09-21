# flask login and registration project 

## 1. Getting Started
There are a few steps we need to take before we create our python login and registration system, we need to download and set up Python and the packages we're going to use.

### 1.1. What You Will Learn in this Tutorial
* Form Design — Design a login and registration form with HTML5 and CSS3.
* Templates — Create Flask templates with HTML and Python.
* Basic Validation — Validating form data that is sent to the server (username, password, and email).
* Session Management — Initialize sessions and store retrieved database results.
* MySQL Queries — Select and insert records from/in our database table.
* Routes — Routing will allow us to point our URL's to our functions.

### 1.2. Requirements
* Download and install Python, for this tutorial I'll be using Python 3.7.2, make sure to check the box Add Python to PATH on the installation setup screen.
* Download and install MySQL Community Server and MySQL Workbench, you can skip this step if you already have a MySQL server set up.
* Install Python Flask with the command: pip install flask
* Install Flask-MySQLdb with the command: pip install flask-mysqldb

### 1.3. File Structure & Setup
We need to create our project directory and files, you can put the directory anywhere on your computer, as long as Python can access it, create the directories and files below.

## File Structure
*pythonlogin > main.py > static >> style.css > templates >> index.html >> register.html >> home.html >> profile.html >> layout.html 
 
  
    
## The below instruction will start your web server (Windows):
* Make sure your MySQL server is up and running, it should have automatically started if you installed it via the installer.
* Open Command Prompt, make sure you have the project directory selected, you can do this with the command cd c:\your_project_folder_destination on Windows.
* Run command: set FLASK_APP=main.py
* Run command: set FLASK_DEBUG=1
* Run command: flask run
* Debug mode will allow us to edit our files without constantly restarting the web server.

## 2. Creating the Database and setting-up Tables
* MySQL Workbench is a GUI for creating and editing our databases, follow the below instructions.
* Open MySQL Workbench
* Fill out your MySQL details
* Click Test Connection, if successful you can click OK
* Open your connection

## Execute the following SQL statements:

CREATE DATABASE IF NOT EXISTS `pythonlogin` DEFAULT CHARACTER SET utf8 COLLATE utf8_general_ci;
USE `pythonlogin`;

CREATE TABLE IF NOT EXISTS `accounts` (
	`id` int(11) NOT NULL AUTO_INCREMENT,
  	`username` varchar(50) NOT NULL,
  	`password` varchar(255) NOT NULL,
  	`email` varchar(100) NOT NULL,
    PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=2 DEFAULT CHARSET=utf8;

INSERT INTO `accounts` (`id`, `username`, `password`, `email`) VALUES (1, 'test', 'test', 'test@test.com');

# After That above Code Use Properly ...
