##Creating a MySql Database

From the MySql shell

\connect

\status

\sql

CREATE DATABASE book_store;

USE book_store;

CREATE TABLE book(id INT PRIMARY KEY 

AUTO_INCREMENT, title VARCHAR(255) NOT NULL, author 

VARCHAR(1000), price DECIMAL(5,2) );

DESCRIBE book;

INSERT INTO test3(title, author, price) VALUES 

("1986", "Julie Carlson test4", 5.00);

SELECT * FROM book;


From the MySQL workbench

Create a new schema in the connected server

Use the Query pane to execute SQL commands
