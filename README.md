# Model for a backend project
This project is based on the tutorial of [Amigos code](https://link-url-here.org) and is a model for study.

The structure of the application has three layers:
* Controller, where the data is exchanged with the user;
* Service layer,  where the business logic is stored;
* Data access layer; where the connection with the database is made.

## How to use.
The application is written to use with the PostgreSQL database. The configuration files
are:
1) src/main/resources/db/migration/V1_PersonTable.sql
The creation of the table.
2) src/main/resources/application.yml
The username, password, database's name, and port number.

Therefore, create an instance of the PostgreSQL with the name and the password listed at the port number registered. I used Docker as a container.

The requests registered are: GET, POST, and PUT, according to the controller class in
src/main/java/dev/andre/myproject/api/PersonController.java.

* GET all elements: GET request to local:8000/api/v1/person
* GET an element by id: GET request to local:8000/api/v1/person/ {id}
* UPDATE an element by id: PUT request to local:8000/api/v1/person/ {old id}
and a body:
{ 
'id': 'new UUID number',
'name': 'name of the element'
}


