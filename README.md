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
