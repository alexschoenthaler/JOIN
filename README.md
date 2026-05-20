# Join

Join is a browser-based Kanban and contact management tool for organizing tasks, priorities, and team contacts. The project is built as a static frontend application using HTML, CSS, and vanilla JavaScript, and uses Firebase Realtime Database as the data source for users, contacts, and tasks.

## Features

- Login with a user account or guest access
- Registration for new users
- Summary dashboard with key metrics and deadlines
- Kanban board with task status, search, and detail view
- Create, edit, and move tasks
- Priorities, subtasks, and contact assignment
- Contact management with create, edit, and delete functionality
- Responsive layouts for desktop and mobile

## Tech Stack

- HTML5
- CSS3
- Vanilla JavaScript
- Firebase Realtime Database

## Project Structure

```text
Join/
|- index.html              # Login
|- signup.html             # Registration
|- summary.html            # Dashboard
|- board.html              # Kanban board
|- add_task.html           # Create tasks
|- contacts.html           # Contact management
|- JS/                     # Page logic and feature modules
|- style/                  # Page and component styles
|- templates/              # Reusable HTML templates
|- assets/                 # Icons, images, and fonts
```

## Local Setup

The project should be started through a local web server, not directly via file://. This is necessary because templates and data are loaded using fetch, for example for the header, sidebar, and Firebase connections.

### Option 1: Live Server in VS Code

1. Open the project folder in VS Code
2. Use the Live Server extension
3. Start index.html through the local server

### Option 2: Simple HTTP Server

If Python is installed:

```bash
python -m http.server 8000
```

Then open in your browser:

```text
http://localhost:8000
```

## Getting Started

After starting the project, the flow begins on the login page:

- index.html: Login and guest access
- signup.html: Create a new user account
- summary.html: Overview of open and urgent tasks
- board.html: Manage tasks on the Kanban board
- add_task.html: Create new tasks
- contacts.html: Manage contacts

## Data Storage

The application connects directly to Firebase Realtime Database. Among others, it uses database sections for:

- LoginData
- Contacts
- Tasks

The Firebase URL is defined in several places throughout the project, including:

- script.js
- JS/signup.firebase.js
- JS/contacts/contacts.config.js
- JS/addTask/addTask.js
- JS/boardandTask/board.core.js
- JS/summary.js

If you want to run the project with your own Firebase database, these endpoints need to be adjusted accordingly.

## Special Notes

- Session data such as login status, username, and guest mode is managed via sessionStorage.
- Header and sidebar are loaded dynamically from templates.
- The application includes protection logic for unauthenticated access to internal pages.

## Project Goal

Join is designed as a compact task management application focused on clear task distribution, visual status tracking, and simple contact management within a team.