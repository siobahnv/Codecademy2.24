# Codecademy Coursework

## Learn Express
"Express is a powerful but flexible Javascript framework for creating web servers and APIs." <br>
CRUD: Create, Read, Update, Delete <br>

## Learn Express Routes
Express is a Node module. <br>
```
// Create a server
const express = require('express');
const app = express();

// Tell it where to listen for requests
const PORT = 4001;
app.listen(PORT, () => {
  console.log(`Server is listening on port ${PORT}`);
});
```
routes, "define the control flow for requests based on the request’s path and HTTP verb." <br>
"The _path_ is the part of a request URL after the _hostname_ and _port number_" <br>
"The HTTP verb is always included in the request" <br>
```
// routes  to register GET requests
app.get(path, callback_function);
```

### End of free part of course