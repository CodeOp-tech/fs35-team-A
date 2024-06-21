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

0. Clone the repository on your local machine and open it.

```javascript
git clone "githublink"
```

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

The database consists of three main tables: `users`, `workouts`, and `exercises`. Below is a summary of their purpose and relationships:

1. **Users Table**

   - **Purpose:** Stores user information.

2. **Workouts Table**

   - **Purpose:** Stores workout sessions, linked to the users who perform and send them.

3. **Exercises Table**

   - **Purpose:** Stores exercises associated with specific workouts.

### Relationships

<<<<<<< HEAD
### Endroutes

- Click here to see the http method, description, request and response objects for each of our endroutes.
  https://docs.google.com/document/d/1VD0Nsywif69Nr0MCx-je22KXIx5FMICRA2M1A-4CoNg/edit
||||||| 99abd21
### Example Queries
=======
1. **Users to Workouts (1:N)**

   - **Relationship:** One user can have multiple workouts.
   - **Details:** The `user_id` column in the `workouts` table references the `id` column in the `users` table.

2. **Users to Workouts (1:N) via `sender_id`**

   - **Relationship:** One user can send or create multiple workouts.
   - **Details:** The `sender_id` column in the `workouts` table references the `id` column in the `users` table.

3. **Workouts to Exercises (1:N)**
   - **Relationship:** One workout can have multiple exercises.
   - **Details:** The `workout_id` column in the `exercises` table references the `id` column in the `workouts` table.

### Summary of Relationships

- **Users to Workouts (user_id):** One user (`users.id`) can have many workouts (`workouts.user_id`).
- **Users to Workouts (sender_id):** One user (`users.id`) can send many workouts (`workouts.sender_id`).
- **Workouts to Exercises:** One workout (`workouts.id`) can include many exercises (`exercises.workout_id`).

These relationships ensure that each workout is linked to a specific user and can include multiple exercises, and they allow tracking of both the user performing the workout and the user who created it.

### Example Queries
>>>>>>> master

The following SQL queries demonstrate how to interact with the database:

1. This query retrieves all workout sessions associated with a specific user, identified by their user_id.

```sql
 SELECT * FROM workouts WHERE user_id = 'specific_user_id';
```

2. This query retrieves all exercises included in a specific workout session, identified by its workout_id

```sql
 SELECT * FROM exercises WHERE workout_id = 'specific_workout_id';
```

3. This query retrieves all workout sessions created by a specific user, identified by their sender_id.

```sql
SELECT * FROM workouts WHERE sender_id = 'specific_user_id';
```

These queries provide insights into how data is structured and retrieved within the database, facilitating understanding of the relationships between users, workouts, and exercises.

## Routes

### End Points

### API Route

<<<<<<< HEAD
||||||| 99abd21
- Enpoints description
- We can create a PDF file and link it

=======
- Enpoints description
- We can create a PDF file and link it

### Guards

>>>>>>> master
## Future Features

### Instructions to contribute

To contribute to this project, follow these steps:

1. **Fork the Project**: Click on the "Fork" button at the top right corner of the repository page on GitHub. This creates a copy of the project under your GitHub account.

2. **Create your Feature Branch**: Switch to your terminal or command prompt and create a new branch for your feature using the following command:

   ```bash
   git checkout -b feature/YourName
   ```

3. **Commit Your Changes**: Make your changes to the project code, then stage and commit the changes using the following commands:

   ```bash
   git add .
   git commit -m 'add descriptive name for your feature'
   ```

4. **Push to the Branch**: Push your local changes to your forked repository on GitHub:

   ```bash
   git push origin feature/YourName
   ```

5. **Open Pull Request**: Go to the GitHub repository page of the original project. GitHub should display a prompt to create a pull request from your recently pushed branch. Follow the prompts to compare changes, write a pull request description, and submit it.

## Contact

- Giulia Cellerino - giulia.cellerino@icloud.com
- Chardae Schnabel - chardaeschnabel@gmail.com

## Acknowledgements

- TA [Pia Prozesky](https://www.linkedin.com/in/pia-prozesky)
- TA [Zoe Laventhol](https://www.linkedin.com/in/zoe-laventhol)
- Teacher [Germinal Camps](https://es.linkedin.com/in/germinal-camps)
