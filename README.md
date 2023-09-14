# simple-crud-golang

#  SETTING UP THE APPLICATION ON YOUR SYTETM 

# To run the application, make sure you have the following prerequisites:

# installed GO on your system.
# SETUP MySQL database server up and run it .

# Update your db details stored in a .env file 

Clone the project from GitHub:

# git clone <repository-url>

# Install the required packages to run the Go application:

# go get github.com/gin-gonic/gin
# go get github.com/go-sql-driver/mysql
# go get github.com/joho/godotenv
# Run the application:
# go run main.go


# Here is my API Documetation 
# it contains all the sample payload and request to access each endpoint 
# https://documenter.getpostman.com/view/11674215/2s9YC4VtXD

# Also below is sample request and reponse format
# Standard Request and Response Formats

Create person.
Request Format:

Method: POST
Endpoint: /api
Request Body: JSON object with the following fields:
"name" (string): The name of the person.
"track" (string): the teack the persoon belong to.
"gender" (string): the gender of the person.
"age" (int): The age of the person.

Example Request:
{
    "name":"olayinka ade ayobami",
    "track": "backend",
    "gender":"male",
    "age":"20"
}

Response Format:

HTTP Status Code: 201 (Created)
Response Body: JSON object with the newly created person:

{
    "name":"olayinka ade ayobami",
    "track": "backend",
    "gender":"male",
    "age":"20"
}

Get Person by ID (GET)
Request Format:

Method: GET
Endpoint: /api/:id
URL Parameter:
id (int): ID of the person to retrieve.
Example Request:
/api/1
Response Format:

HTTP Status Code: 200 (OK)
Response Body: JSON object with the person's details:
{
   "name":"olayinka ade ayobami",
    "track": "backend",
    "gender":"male",
    "age":"20"
}
Update Person by ID (PUT)
Request Format:

Method: PUT
Endpoint: /api/:id
URL Parameter:
id (int): ID of the person to update.
Request Body: JSON object with the updated fields:
"name" (string): The updated name of the person.
"track" (string): the updated teack the persoon belong to.
"gender" (string): the updated gender of the person.
"age" (int): The updated age of the person.
Example Request:
/api/1
{
    "name":"olayinka ade ayobami",
    "track": "backend",
    "gender":"male",
    "age":"40"
}
Response Format:

HTTP Status Code: 200 (OK)
Response Body: JSON object with the updated person:
{
    "name":"olayinka ade ayobami",
    "track": "backend",
    "gender":"male",
    "age":"40"
}
Delete Person by ID (DELETE)
Request Format:

Method: DELETE
Endpoint: /api/:id
URL Parameter:
id (int): ID of the person to delete.
Example Request:
/api/2
Response Format:

HTTP Status Code: 200 (OK)
Response Body: JSON object with a success message:

{
    "message": "Successfully deleted"
}



