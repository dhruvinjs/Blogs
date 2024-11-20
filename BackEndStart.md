#THis file will contain All the details About TO start your backend proj

npm init 
WIll initialize a package for the folder 
It weil ask you simple question like packagge name 
GIt name 
author
Note=If you are a eginner do not write anything in the test folder



To start your server 
npm start

Then  Install important libraries for your project
##Express.js 
command=npm i express
Handle Requests: You can easily set up ways to respond to users visiting your website or using your API.
Add Features: Quickly add things like user authentication or data handling without writing lots of code.
Save Time: It simplifies tasks so you can build your project faster.

##Nodemon
command= npm i nodemon
Whenever you make a change it automatically restarts your server so that changes are refelcted on the server
Easy to Use: Just replace node with nodemon when running your script, and it handles everything for you.
To use nodemon in your project]
Open your package.json file.

##Look for the scripts section.
Change "node app.js" to "nodemon app.js":
"scripts": {
  "start": "nodemon app.js"
}


##JSON-WEB-TOKEN (jwt)
Secure Login: It lets you send information between the server and the client in a way that nobody can change or tamper with.
Simple to Use: It’s easy to create, send, and check tokens for login or authorization.
command=npm i jsonwebtoken

These is simple code snippet which will create ! folder
SRC Source folder which will contain the source code
## 5 Subfolders
Models
The models folder is where you define the structure of your data. It tells your application what kind of information to expect and how it should be stored in the database.

For example:

If you're making a "User" model, you'd define things like name, email, and password as parts of a user's data.
You can also add functions that help you do things like save or find users in the database.


Middleware
The middleware folder contains functions that act like a checkpoint before a request reaches the main part of your app (the controller).

For example:

It can check if a user is logged in before letting them access certain pages.
It can also log details about each request or check if the data sent is correct.

db:

Manages the connection to your database and stores related functions like setting up a database connection.
Example: A file in this folder could handle connecting to MySQL, MongoDB, or any other database system you're using.

controllers:

Contains functions that handle incoming requests and perform actions like fetching data, processing information, or returning responses.
Example: A UserController might handle actions like creating a user, updating user info, or deleting a user.


const fileStructure=require("fs")

const folders=['controllers','middleware','routes','utils','db','models']
folders.forEach((values)=>
{
    fileStructure.mkdir(`./src/${values}` ,{recursive:true}, err=> err ? console.error(err) : console.log("success"))
}
)
This is the simple code sniipet you can use to make your backend project


## Mongoose 
command npm i mongoose
mongoose will help you to connect mongo DB
It will also help you to create models 

## Bcrypt 
command npm i bcrypt 
it will you to hash the password when you are storing in the database

## GITIGNORE 
In this file you will be adding the ile enames which you want git to track like .env file
node_modules folder




## ENV File 
This is the important file which you have to create Because in this file you will store your information 
Example = Secret api keys 

## DOTENV Package 
THis will be the package which wil =you to configure your .env file
NOTE= Never push your .env file to an open source project wiht the code
Command =npm i dotenv

##Index.js file code 

import dotenv from "dotenv"
import express from "express";

const app=express()
dotenv.config({
    path:'./.env'
})

const port=process.env.PORT
app.listen(port,()=>console.log(`Listening in ${port}`))

This can be your code for your index file to setup the project

This are the basic steps you can take for setting up a node js project 
After this create models then connect your database and setUp login logout


##  Other than this FIGURE OUT YOURSELF