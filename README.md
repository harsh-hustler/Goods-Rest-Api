# Warehouse-Rest-Api(Flask, Flask-RESTful, Flask-JWT, Flask-SQLAlchemy, PostgreSQL, SQLite, Postman)

Warehouse-Rest-Api is a RESTful API made in **flask** to provide user a experience of how warehouse, inventory works.

  - Allows user to **Register** for free and added user authentication at get end point using JWT token.
  - Allows user to create, delete and get a list of Store.
  - Allows user to create items by mapping it to a specific store using store id.
  - Also have the powerpack feature comprised of getting a specific item, list of all the items, update and delete an item.
  - Used advanced Request parsing with flask RESTful

# Features

  - Setted some test cases at various end point to pass using advanced postman environment. If the test cases doesn't pass, then the execution of that end point gets terminated automatically with a proper message.
  - Restricted the same user, item, store to enter again with a proper and valid error code.
  - Bifurcated into models, resources folder to improve the project structure and make it flawless.
  - Implemented using GET, POST, PUT and DELETE http request protocol.

![Screenshot (968)](https://user-images.githubusercontent.com/78041915/110780167-6a924280-828a-11eb-9a87-44f1a5041429.png)
![Screenshot (969)](https://user-images.githubusercontent.com/78041915/110780170-6bc36f80-828a-11eb-96f5-2dc248bacced.png)
![Screenshot (970)](https://user-images.githubusercontent.com/78041915/110780172-6c5c0600-828a-11eb-8489-0f00ed96a095.png)
![Screenshot (971)](https://user-images.githubusercontent.com/78041915/110780175-6cf49c80-828a-11eb-8350-8e2539b24ba0.png)
![Screenshot (972)](https://user-images.githubusercontent.com/78041915/110780177-6cf49c80-828a-11eb-9d98-bb7c36eb281f.png)
![Screenshot (972 1)](https://user-images.githubusercontent.com/78041915/110780180-6d8d3300-828a-11eb-8fe7-b977611a99c6.png)
![Screenshot (973)](https://user-images.githubusercontent.com/78041915/110780181-6e25c980-828a-11eb-98ac-e9c4a93c1b65.png)
![Screenshot (974)](https://user-images.githubusercontent.com/78041915/110780184-6ebe6000-828a-11eb-8d2a-bd84158d069a.png)
![Screenshot (975)](https://user-images.githubusercontent.com/78041915/110780187-6f56f680-828a-11eb-843b-4fd86cb03ca4.png)
![Screenshot (976)](https://user-images.githubusercontent.com/78041915/110780188-6f56f680-828a-11eb-9236-5fdc0bbf9784.png)
![Screenshot (977)](https://user-images.githubusercontent.com/78041915/110780192-6fef8d00-828a-11eb-95af-f00415114dee.png)
![Screenshot (978)](https://user-images.githubusercontent.com/78041915/110780194-70882380-828a-11eb-89ca-7c24a5e37c72.png)
![Screenshot (979)](https://user-images.githubusercontent.com/78041915/110780196-7120ba00-828a-11eb-9e42-0f712f6bf80b.png)
![Screenshot (980)](https://user-images.githubusercontent.com/78041915/110780201-7120ba00-828a-11eb-983a-7fa75c4661cd.png)
![Screenshot (981)](https://user-images.githubusercontent.com/78041915/110780203-71b95080-828a-11eb-8a78-4e7b62c6ffe2.png)
![Screenshot (982)](https://user-images.githubusercontent.com/78041915/110780205-7251e700-828a-11eb-8be6-9bbddef4f565.png)
![Screenshot (983)](https://user-images.githubusercontent.com/78041915/110780207-72ea7d80-828a-11eb-8033-049923d4cef0.png)



## There is only one branch in this repository i.e `master`  branch

### For `master` branch
* For Flask 1+
* Works with Python 3.9+

```
The template structure is as follows:
├── app.py    <-contains all the apps for the project. New apps should be added to this particular package only.
├── db.py     <-to host SQLAlchemy object
├── models    <-internal representation of an entity
│   ├── __init__.py     <-making folder as package and telling python to look inside these folders for python files.
│   ├── item.py
│   ├── store.py
│   └── user.py
├── Procfile            <-procfile for heroku
├── requirements.txt    <-required libraries to install for deploying in heroku.
├── resources           <-external representation of an entity
│   ├── __init__.py     <-making folder as package and telling python to look inside these folders for python files.
│   ├── item.py        
│   ├── store.py
│   └── user.py
├── run.py              <-python file to import db.
├── runtime.txt         <-telling heroku the python version
├── security.py         <-setted authentication and validated user.
└── uwsgi.ini           <-configuration parameters for the uwsgi process to run the app
```

# How to Install and run

### To run locally
```
$ mkdir my_project
  --template=https://github.com/harsh-hustler/Warehouse-Rest-Api/archive/master.zip
  --extension=py
$ sudo apt install python3-pip
$ pip3 install flask
$ pip3 install flask_restful
$ pip3 install flask-jwt
$ pip3 install Flask-SQLAlchemy
$ python app.py
$ postman .
```
It is considered good practice to run the above commands in a new and separate virtual environment. Read more about virtual environments [here](https://realpython.com/python-virtual-environments-a-primer/).

# Deployment

## To run on cloud i.e.Remote Server
The project template contains the `Procfile` for deploying it to Heroku. Within your project directory, run the following commands in the sequence they appear.

```
$ heroku create
$ heroku addons:add heroku-postgresql:hobby-dev
$ git push heroku master
$ pip freeze > requirements.txt
$ heroku run
$ heroku open
```
**Copy the URL and change the url in postman from local server url to the copied url and you will be good to go.**

Also, do not forget to set the project environment variables.

You should have a Heroku account (if not, create one [here](https://www.heroku.com/)), and Heroku CLI installed for the commands to work (if not, installation instructions can be found [here](https://devcenter.heroku.com/articles/heroku-cli)).
