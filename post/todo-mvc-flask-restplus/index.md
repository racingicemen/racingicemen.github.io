> An introduction to building REST applications using Flask-RESTPlus, Flask-SQLAlchemy

In this blog post, I will go through the steps in building a simple ToDo application using
[Flask](http://flask.pocoo.org) and [Flask-RESTPlus](https://github.com/noirbizarre/flask-restplus). This
post is based on the [quickstart tutorial](http://flask-restplus.readthedocs.io/en/stable/quickstart.html)
except we will be plugging in to [PostgreSQL](http://postgresql.org) via 
[Flask-SQLAlchemy](http://flask-sqlalchemy.pocoo.org). Finally, the front end will be done in 
[Elm](http://elm-lang.org)

# Design
First let's look briefly at the design of the TodoMVC application.

## Static Structure 
![image](/static/todo-mvc-flask-restplus-todo-todolist.png)

The ```ToDoList``` class manages the CRUD operations for the application. 

A ```ToDo``` consists of

* ```description```: a string describing the task.
* ```status```: the status of the todo item --- ```inactive```, ```active```, ```completed```, ```overdue```
* ```due_datetime```: the due date and time for the todo item.

## Dynamic Structure
![image](/static/todo-mvc-flask-restplus-sequence.png)