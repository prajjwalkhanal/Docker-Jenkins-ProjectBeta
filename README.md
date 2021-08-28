## Simple app - developing with Docker

This  app shows a simple user sign up using docker
- index.html with pure js and css styles
- nodejs backend with express module
- mongodb for data storage

All components are docker-based


#### To start the application

Step 1: start mongodb and mongo-express

    docker-compose -f docker-compose.yaml up
    
_You can access the mongo-express under localhost:8080 from your browser_
    
Step 2: in mongo-express UI - create a new database "my-db"

Step 3: in mongo-express UI - create a new collection "users" in the database "my-db"       
    
Step 4: start node server 

    npm install
    node server.js

    Or docker image from the application

    docker build -t my-data-app:1.0 .       
    
    The dot "." at the end of the command denotes location of the Dockerfile.
    
    docker run -d -p 3000:3000 --network=data-app-nwt my-data-app:1.0

Step 5: access the nodejs application from browser 

    http://localhost:3000
