#code coverage

[![codecov](https://codecov.io/gh/aflouat/Bob-APP-P10-CI-CD/branch/main/graph/badge.svg)](https://codecov.io/gh/aflouat/Bob-APP-P10-CI-CD)

# BobApp

Clone project:

> git clone https://github.com/aflouat/Bob-APP-P10-CI-CD.git

## Front-end 

Go inside folder the front folder:

> cd front

Install dependencies:

> npm install

Launch Front-end:

> npm run start;

### Docker

Build the container:

> docker build -t bobapp-front .  

Start the container:

> docker run -p 8080:8080 --name bobapp-front -d bobapp-front

## Back-end

Go inside folder the back folder:

> cd back

Install dependencies:

> mvn clean install

Launch Back-end:

>  mvn spring-boot:run

Launch the tests:

> mvn clean install

### Docker

Build the container:

> docker build -t bobapp-back .  

Start the container:

> docker run -p 8080:8080 --name bobapp-back -d bobapp-back 
