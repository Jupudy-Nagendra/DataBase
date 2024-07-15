# DataBase
## Implementing CRUD Operations with MySQL and FastAPI

**Step-1**
MYSQL WorkBench
1. Create a local Connection in MYSQL with
   userid: root
   password: 123456
2. Create a database school
   command: create database school;
   command: use school;
3. create a table called students
   command:
   CREATE TABLE students (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    age INT NOT NULL,
    grade VARCHAR(10) NOT NULL
    );

**Step-2**
1. Download the main.py and database.py files from the MYSQL folder
2. Keep the both files in a same folder
3. Open in VS studio and select the desired folder (set path)
4. run the python terminal
5. initiate the fastapi (run)
   Command :
   uvicorn main:app --reload
   or
   fastapi dev main.py
6. FASTAPI connection is established

**Step-3**
Test the application
1. Open the postman application and use the below commands for operation
2. Commands
   **Get Command**
    curl -X 'GET' \
      'http://127.0.0.1:8000/students/' \
      -H 'accept: application/json'

    **Create an entry**
    curl -X 'POST' \
      'http://127.0.0.1:8000/students/' \
      -H 'accept: application/json' \
      -H 'Content-Type: application/json' \
      -d '{
      "name": "string",
      "age": 0,
      "grade": "string"
    }'
    
    **Get by unique id**
    curl -X 'GET' \
      'http://127.0.0.1:8000/students/1' \
      -H 'accept: application/json'
    
    **Update**
    curl -X 'PUT' \
      'http://127.0.0.1:8000/students/1' \
      -H 'accept: application/json' \
      -H 'Content-Type: application/json' \
      -d '{
      "name": "string",
      "age": 0,
      "grade": "string"
    }'
    
    **Delete**
    curl -X 'DELETE' \
      'http://127.0.0.1:8000/students/1' \
      -H 'accept: application/json'






















