# Server
# In Angular Form you have create one folder:-
 
 folder name:-server
 
 # In cmd or terminal you have to open another cmd window:-
 	npm init --yes   (press enter)
 
 # Install the dependency:-
 	npm install --save express body-parser cors
 	
 	:- Express in the web server 
 	:- body-parser - body-parser is a middleware to handel form data 
 	:- cors:- cors is a package to make request aquarce different codes
 	
  # create one file :- file name- server.js
 	
 	
const express = require('express');
const bodyParser = require('body-parser');
const cors = require('cors');

const PORT = 3000;

const app = express();

app.use(bodyParser.json());

app.use(cors());

app.get('/', function(req, res){
    res.send('Hello from server')
})

app.post('/enroll', function(req, res){
    console.log(req.body);
    res.status(200).send({"message": "Data received"})
})

app.listen(PORT, function(){
    console.log("Server running on localhost:" + PORT);
});

# after this code you can run the command in terminal

TYPE:-
	node server
LIKE THIS:-

	:-vijaya@vijaya-OptiPlex-755:~/Desktop/Angular/Angular-Forms/server$ node server
        :-Server running on localhost:3000
        
# then you can run the tdf project ng serve 

	and fill form and submit then 
	-you have to open console :-
		Success! 
Object { message: "Data received" }
