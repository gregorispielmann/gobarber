<!--<p align="center">
  <a href="" rel="noopener">
 <img width=200px src="https://github.com/Rocketseat/bootcamp-gostack-desafio-02/raw/master/.github/logo.png" alt="Project logo"></a>
</p>-->

<h3 align="center">Gobarber</h3>

<div align="center">

[![Status](https://img.shields.io/badge/status-active-success.svg)]()
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](/LICENSE)

</div>

---

<p align="center"> This app is a full barber manager called Gobarber.
<br>
In this challenge was built some basic funcionalities to the barber manager and clients.  The concept was a web app to barbers control schedules made by clients. After we made a Mobile App (iOS Only) for the clients do schedules at the barbers. 
    <br> 
</p>

## 📝 Table of Contents

- [About](#about)
- [Getting Started](#getting_started)
- [Usage](#usage)
- [Built Using](#built_using)
- [Authors](#authors)
- [TODO](#todo)

## 🧐 About <a name = "about"></a>

This project was made to be a full stack application including front-end, back-end and mobile.

## 🏁 Getting Started <a name = "getting_started"></a>

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

What things you need to install the software and how to install them.

- [Docker](https://www.docker.com/) - Container Platform
- [Yarn](https://yarnpkg.com/lang/en/) - Package Manager

### Installing

A step by step series of examples that tell you how to get a development env running.

### Cloning Repo

```
$ git clone https://github.com/gregorispielmann/gobarber.git
```

### Containers

First of all you need to create the containers (Postgres and redis), after install docker run the following command on your terminal

**IMPORTANT! Replace ???? by an available port**

```
$ docker run --name gobarber -e POSTGRES_PASSWORD=docker -p ????:5432 -d postgres:11
To create the container for Postgres DB

And then

$ docker run --name redisgobarber -p ????:6379 -d -t redis:alpine
To create the container to Redis

```

### Database

Before run backend you will need create the postgres database in our container. For this I highly recommend you to use [Postbird](https://github.com/Paxa/postbird). Then connect with your information (Postgres container) and create the database with name **'gobarber'** before you go to next step.

### Backend

After create and run all containers, create the postgres database you will be ready to initialize the backend.

Inside the backend folder run commands below.

```
$ yarn
To install all dependencies

$ yarn sequelize db:migrate
To run all migrations to database

$ yarn sequelize db:seed:all
To seed database with fake data
```

**ATTENTION! Before you start the development mode of backend, you will need edit the .envexample to your information and rename the file to .env**

After this you only need to run command below

```
$ yarn dev
This will start backend in dev mode

$ yarn queue
This will start the redis task queue
```

### Frontend (Web)

### Demo

<img src="screenshots/web.gif"/>
<img src="screenshots/screenshot1.png"/>
<img src="screenshots/screenshot2.png"/>
<img src="screenshots/screenshot3.png"/>

### How to run?

After run backend.

```
$ yarn
To install all dependencies

$ yarn start
To run react application
```

### Mobile (:apple: iOS Only)

### Demo

<div style="display: flex;">

<img src="screenshots/ios.gif" width="33%"/>

<img src="screenshots/screenshotios0.png" width="33%"/>
<img src="screenshots/screenshotios1.png" width="33%"/>
<img src="screenshots/screenshotios2.png" width="33%"/>
<img src="screenshots/screenshotios3.png" width="33%"/>
<img src="screenshots/screenshotios4.png" width="33%"/>

</div>

### How to run?

After run backend, inside the mobile folder run commands below.

```
$ yarn
To install all dependencies

$ cd ios && pod instal && cd ..
To install all cocoa pods dependencies

$ react-native run-ios
To run react application
```

## 🎈 Usage <a name="usage"></a>

### Web

Running the app you will signin with login info below

```
Login: demo@prestador.com
Password: demo123
```

### Mobile

You will only need an E-mail and a Password from a client that is not a provider.

## ⛏️ Built Using <a name = "built_using"></a>

- [Docker](https://www.docker.com/) - Container Management
- [Redis](https://redis.io/) - Database
- [Postgres](https://www.postgressql.org/) - Database
- [Sequelize](https://sequelize.org/) - Node.js ORM
- [NodeJs](https://nodejs.org/en/) - Server Environment
- [Express](https://expressjs.com/) - Server Framework
- [ReactJs](https://reactjs.org/) - Web Framework
- [React Native](https://react-native.org/) - Mobile Framework
- [Styled Components](https://www.styled-components.com/) - CSS in Javascript library
- and others

## ✍️ Authors <a name = "authors"></a>

- [@rockeseat](https://rocketseat.com.br/bootcamp) - Idea & Initial template
- [@gregorispielmann](https://github.com/gregorispielmann) - Back-end, Front-end and Mobile App development

## TODO <a name="todo"></a>

- Android mobile app
- Aditional features to web and mobile

## Made with ☕️ and ❤️ by Gregori Spielmann
