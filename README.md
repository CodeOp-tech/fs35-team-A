# Char & Giulia Fitness App

By Chardae Schnabel and Giulia Cellerino

## Table of Contents

- [Introduction](#introduction)
- [Motivation](#motivation)
- [Features & Views](#features-views)
- [Tools Used](#tools-used)
- [Getting Started](#getting-started)
- [Database Schema](#database-schema)
- [Relationships](#relationships)
- [EndRoutes](#endroutes)
- [API Route](#api-route)
- [Future Features](#future-features)
- [Contact](#contact)
- [Acknowledgements](#acknowledgements)

## Introduction

Our app is designed to empower you with confidence and motivation as you embark on your fitness journey.

## Motivation

Giulia and Chardae, like many, often felt gym-intimidated and demotivated at home. Complex routines and lacking guidance made fitness daunting. They saw this shared struggle and the gap in supportive fitness apps.

Traditional apps often lack personalized guidance and motivation. Giulia and Chardae envisioned an app offering tailored workouts, flexible scheduling, and continuous motivation.

This fitness app focuses on building confidence and inspiring users of all levels. They believe everyone deserves empowerment and motivation in their fitness journey. With Char & Giulia Fitness App, users confidently embark, knowing they have a supportive companion every step.

## Features & Pages

This app is made up of the following pages:

- <h2>Homepage:</h2> Provides an overview of the app, featuring essential information and navigation options.

- <h2>Register && Login:</h2> Provides a registration form for new users to create accounts and join the app. Standard Login page - allows users to authenticate and access their accounts securely.

  <img src="client/images/READMEimages/RegistrationPage.png" alt="Home Page" width="500"/>

  The user has the option to upload a photo...

  <img src="client/images/READMEimages/RegisterWithPhoto.png" alt="Home Page" width="500"/>

  And the photo will load in the navbar, when logged in:

  <img src="client/images/READMEimages/NavBarWithPhoto.png" alt="Home Page" width="500"/>

- <h2>Buildyourownworkout:</h2> Enables users to customize their workout routines based on preferences and goals.

   <img src="client/images/READMEimages/BuildYourWorkout.png" alt="Home Page" width="500"/>

  Dropdown menu calls the API in order to provide user with WO options.

  <img src="client/images/READMEimages/WorkoutDropdown.png" alt="Home Page" width="500"/>

- <h2>Workout:</h2> Presents structured workout routines and exercises tailored to user preferences.

 <img src="client/images/READMEimages/WorkoutSummary.png" alt="Home Page" width="500"/>

FullCalendar.io was used in order to give the user the option to choose a day and time...

  <img src="client/images/READMEimages/CalendarDrop.png" alt="Home Page" width="200"/>

- <h2>Profile && Calendar:</h2> Profile includes the option to render profile details, see workouts sent by friends and to organze WOs with a drag and drop option in the Calendar. Displays scheduled workouts and fitness events, helping users plan and track their activities.

<img src="client/images/READMEimages/ProfileCalendar.png" alt="Home Page" width="400"/>

Below the calendar is also a month summary of all of the workouts organized for that month, with each workout rendering a separate delete or edit workout option.

<img src="client/images/READMEimages/SummaryOfMonth.png" alt="Home Page" width="300"/>

- <h2>**Exercise:**</h2> Offers detailed information and instructions for various exercises and workout routines, as well as a progress bar to movivate the user (and so they know where they are in their routine)!

<img src="client/images/READMEimages/ExerciseNow.png" alt="Home Page" width="300"/>

- <h2>Sentworkouts:</h2> Shows a history of sent or scheduled workout plans, facilitating organization and planning.

<img src="client/images/READMEimages/SentWorkouts.png" alt="Home Page" width="500"/>

- <h2>Sidebar:</h2> Provides quick access to navigation options and additional features throughout the app.

## Tools Used

- **VS Code** - Source code editor
- **Github** - Version control platform
- **Gitbash** - Command line interface for Git
- **Postman** - API development and testing
- **MySQL** - Relational database management system
- **HTML** - Markup language for creating web pages
- **CSS** - Stylesheet language for styling web pages
- **JavaScript** - Programming language for web development
- **React.js** - JavaScript library for building user interfaces
- **Bootstrap** - Front-end framework for responsive web design
- **Node.js** - JavaScript runtime environment
- **Express** - Web application framework for Node.js
- **JWT** - JSON Web Tokens for authentication
- **Bcrypt** - Password hashing function
- **Trello** - Project management tool for organizing tasks
- **DrawSQL** - Tool for creating database diagrams
- **FullCalendar.io** - JavaScript calendar library for displaying events
- **Material-UI** - React component library for building UIs with Google's Material Design principles
- **Exercise API** - API for retrieving exercises and workout data from:
  [Ninja API](https://api-ninjas.com/api/exercises)

## Getting Started

### Prerequisites

Before you begin, ensure you have the following installed on your local machine:

- [Node.js](https://nodejs.org/) - JavaScript runtime environment
- [npm](https://www.npmjs.com/) - Package managers for Node.js
- [MySQL](https://www.mysql.com/) - Relational database management system
- [Exercise API](https://api-ninjas.com/api/exercises) - Obtain your API key from the website.

### Installation

1. You need to create two (2) .env files.

- This .env goes in the client folder, as it contains the API Key accessible in the frontend

```javascript
VITE_RAPIDID_API_KEY = "Your_API_KEY";
```

- This .env goes in the root project folder

```javascript
DB_HOST = localhost;
DB_USER = root;
DB_NAME = fitnessapp;
DB_PASS = root;
SUPER_SECRET = your_supersecret;
```

2. Run the database

- Open a tab in your terminal and run:

```mySQL
mysql -u root -p
```

3. Create a new database called fitnessapp

```mySQL
CREATE DATABASE fitnessapp
```

4. Install NPM packages on both the server and on the client.

```javascript
cd fs35-team-A //or any name you have given //
npm install
cd client
npm install
```

5. Populates the database with the correct information.

```javascript
npm run migrate
```

6. To run the backend:

```javascript
npm start
```

7. To run the frontend:

```javascript
cd client
npm run dev
```

Frontend runs on http://localhost:5173/, and backend runs on http://localhost:4000.

## Database Schema

![Database Schema Diagram](/client/images/READMEimages/DatabaseSetup.png)

### Relationships

### Endroutes

- Click here to see the http method, description, request and response objects for each of our endroutes.
  https://docs.google.com/document/d/1VD0Nsywif69Nr0MCx-je22KXIx5FMICRA2M1A-4CoNg/edit

## API Route

## Future Features

### Instructions to add future features

## Contact

- Giulia Cellerino - giulia.cellerino@icloud.com
- Chardae Schnabel - chardaeschnabel@gmail.com

## Acknowledgements

- TA Pia Prozesky
- TA Zoe Laventhol
- Teacher Germinal Camps
