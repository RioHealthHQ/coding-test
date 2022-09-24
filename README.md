# Coding Test for Node.Js / Full-stack Developer

As a NodeJS developer in your company, you have been assigned a task to create a simple HTTP web server using only the HTTP core module.
 
Each project is a JSON entry with the following keys:

	id: The unique ID of the project.
	name: The name of the project.
 
Note: A file with an array of projects, data-store.js, is present in the root of the project. Import the data from this file.

```
// index.js

var projects = require('./data-store');

// For GET requests, send the data from the projects array. 


// Write your server logic here
```

## Detailed Requirements


- The web server should be created using only the native `HTTP module`.

- Accept requests for the GET /projects/:id endpoint, where id is the value passed in the URL. If the ID value is not set or is empty in the URL, the server responds back with the status code 400 and the JSON message {"message" : "BAD REQUEST"}.

- If the ID is valid, filter the projects list based on the ID passed as input to the endpoint such that project id matched the input passed. The server sends a JSON response back with the filtered project data, along with the status code 200.

- If the ID is valid but no matching projects are found for the ID, the server responds with the status code 404.

- If the request to the web server contains a route other than /projects, the server responds back with the status code 404.

- Make sure that the server is listening for requests on port 8000. External tools will not be able to be connected to any port other than 8000.
