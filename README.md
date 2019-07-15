# Restful-Api-With-Python-and-Flask
Build Simple Restful Api With Python and Flask

In this article I will show you how to build simple restful api with flask and SQLite that have capabilities to create, read, update, and delete data from database.
I have tested the code presented in this article on python 2.7, though it likely be okay on python 3.4 or newer. Also I assume you have installed flask on your computer, I have explained this step on part 1.
a. Installing flask-sqlalchemy and flask-marshmallow
SQLAlchemy is python SQL toolkit and ORM that gives developer the full power and flexibility of SQL. Where flask-sqlalchemy is flask extension that adds support for SQLAlchemy to flask application(http://flask-sqlalchemy.pocoo.org/2.1/).
In other hand flask-marshmallow is flask extension to integrate flask with marshmallow(an object serialization/deserialization library). In this article we use flask-marshmallow to rendered json response.
You could installing flask-sqlalchemy and flask-marshmallow easily using pip, with the following command:
  $ pip install flask_sqlalchemy
  $ pip install flask_marshmallow
  $ pip install marshmallow-sqlalchemy
b. Prepare your code
Create new python file on flask_tutorial folder named it crud.py. Write down following code in crud.py.

Generate SQLite database first.
The above code to handle CRUD operation to SQLite, but if you run this python file and try to access the endpoint(you can try to access localhost:5000/user) you will get the error message similar with
OperationalError: (sqlite3.OperationalError) no such table: user [SQL: u’SELECT user.id AS user_id, user.username AS user_username, user.email AS user_email \nFROM user’]
This error message occurred because you trying to get data from SQLite, but you don’t have SQLite database yet. So In this step we will generate SQLite database first before running our application. You can generate SQLite database based on your model in crud.py using following step.
enter into python interactive shell
First you need to enter into python interactive shell using following command in your terminal:
  $ python
2. import db object and generate SQLite database
Use following code in python interactive shell

  >>> from crud import db
  >>> db.create_all()

And crud.sqlite will be generated inside your flask_tutorial folder.
d. Run flask application
Now after generate sqlite database, we are ready to run our flask application. Run following command from your terminal to run your application.
  $ python restful_curd.py
