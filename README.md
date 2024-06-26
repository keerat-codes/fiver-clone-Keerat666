
# fiver-clone-Keerat666

A fiver clone




## Installation

Install the dependencies with npm

```bash
  npm install
```



## Running the project locally

Hit npm start

```bash
  npm start
```


## Environment Variables

By default, a dummy connection to the database has been set up in the middleware/connection.js file.

To run this project with your custom TiDB, you will need to add the following connection variables to your .env file.

`user`

`password`

`database`

Then replace the contents of connection.js file with : 

```

var mysql = require("mysql")

var connection = mysql.createConnection({
    host: 'gateway01.eu-central-1.prod.aws.tidbcloud.com',
    port: 4000,
    user: process.env.user,
    password: process.env.password,
    database: process.env.database,
    ssl: {
      minVersion: 'TLSv1.2',
      rejectUnauthorized: true
    }
  });

  module.exports = connection

  ```


## Tech Stack

**Server:** Node, Express


## Hit the first API

Once the code is running successfully on your local. try hitting the following link on your browser : 

```http
  localhost:3008/api/health
```


If it returns a Hello, then you are good to go!

Consult your project overview page to get further details of the API's that are already developed in your project!

The overview page looks something like this on AutoPilot : 

![alt text](https://i.ibb.co/DMWJy0T/Screenshot-2023-07-29-at-4-42-44-AM.png)


### This project was initially auto generated by AutoPilot 🚀

Check out autopilot at : https://autopilot-zgz8.onrender.com



