# prodesk-capstone-taskmatrix
#  TaskMatrix — Agile Project Management Platform

TaskMatrix is an enterprise-style Agile Project Management platform designed to help project managers and team members efficiently manage projects, tasks, assignments, and progress from a centralized dashboard.

The application focuses on providing a clean, responsive, scalable, and user-friendly project management experience.

----

## Project Objective

The main objective of TaskMatrix is to provide teams with a centralized platform where they can:

* Create and manage projects
* Register and authenticate users
* Create and manage tasks
* Assign tasks to team members
* Track task progress
* View project and task information
* Organize tasks using a Kanban board
* Search and filter tasks

---

## Target Users

TaskMatrix will primarily support two user roles.

###  Project Manager

Project Managers can:
* Create projects
* Edit and delete projects
* Create tasks
* Assign tasks
* Set task priority
* Monitor project progress
* Manage project tasks

###  Team Member

Team Members can:
* View assigned tasks
* View task details
* Update task status
* Track their assigned work

---

#  Designated Track
**Track A — Frontend Specialists**
### Focus Areas
* **Component-Driven Development** *(Building the UI using small, reusable components)*
* **Modern Frontend Architecture** *(Organizing the application into a clean and scalable structure)*
* **State Management** *(Managing global application data using Redux Toolkit)*
* **Responsive UI/UX** *(Making the application usable on desktop, tablet, and mobile)*
* **Reusable Components** *(Creating components that can be reused across different screens)*
* **Scalable Project Structure** *(Structuring the project so new features can be added easily)*

---

# 🛠️ Tech Stack

## Frontend

* Next.js
* React
* JavaScript
* HTML5
* CSS

## State Management

* Redux Toolkit
* React Redux

## Backend

* Node.js
* REST API

## Database

* MongoDB

## UI/UX & Architecture

* Figma
* Draw.io

## Version Control & Deployment

* Git
* GitHub
* Vercel

---

# 🚀 Core Features

## 🟢 P0 — Mandatory Features

P0 features represent the minimum functional requirements of TaskMatrix and will be fully implemented.

---

## 1. 🔐 Authentication & Registration

TaskMatrix will provide a basic user authentication system.

### Features

* User Registration / Sign Up
* User Login
* User Logout
* User Roles
* Protected application areas

### Registration Fields

Users will provide:

* Full Name
* Email Address
* Password
* Confirm Password
* User Role

### Authentication Flow

```text
Register
   ↓
Login
   ↓
Dashboard
   ↓
Projects / Tasks
```

---

# 2. 📊 Dashboard

The Dashboard will provide an overview of the user's projects and tasks.

### Dashboard Information

* Total Projects
* Total Tasks
* Completed Tasks
* In Progress Tasks
* Pending Tasks
* Recent Projects
* Recent Tasks

Example:

```text
Total Projects     5
Total Tasks       42
Completed         25
In Progress       10
Pending            7
```

---

# 3. 📁 Project Management

Users with appropriate permissions will be able to manage projects.

### Project Features

* Create Project
* View Projects
* View Project Details
* Edit Project
* Delete Project

### Project Information

Each project may contain:

* Project Name
* Description
* Start Date
* Due Date
* Status
* Project Members
* Tasks

---

# 4. ✅ Task Management

TaskMatrix will allow users to create and manage project tasks.

### Task Features

* Create Task
* View Tasks
* View Task Details
* Edit Task
* Delete Task
* Assign Task

### Task Information

Each task will contain:

* Task Title
* Description
* Assignee
* Priority
* Status
* Due Date
* Project

---

# 5. 🔄 Task Status Management

Tasks will follow a simple Agile workflow.

```text
TODO
  ↓
IN PROGRESS
  ↓
IN REVIEW
  ↓
DONE
```

Users will be able to update the status of tasks according to their workflow.

---

# 🟡 P1 — Selected Features

Only selected P1 features will be implemented to maintain a focused and achievable project scope.

---

# 6. 🗂️ Kanban Board

TaskMatrix will provide a Kanban-style board for visually organizing tasks.

```text
┌────────────┬──────────────┬────────────┬──────────┐
│ TODO       │ IN PROGRESS  │ IN REVIEW  │ DONE     │
├────────────┼──────────────┼────────────┼──────────┤
│ Task 1     │ Task 3       │ Task 5     │ Task 7   │
│ Task 2     │ Task 4       │ Task 6     │ Task 8   │
└────────────┴──────────────┴────────────┴──────────┘
```

The Kanban Board will make task progress easier to visualize.

---

# 7. 🔍 Search & Filters

Users will be able to quickly find and organize tasks.

### Search

* Search tasks by title or keyword

### Filters

* Filter by Status
* Filter by Priority

Example:

```text
Search: Login

Status:
All | TODO | IN PROGRESS | IN REVIEW | DONE

Priority:
All | Low | Medium | High
```

---

# 🔴 P2 — Stretch Goals

P2 features are outside the current capstone implementation scope.

The following features will not be implemented in the current version:

* Notifications
* Advanced Analytics
* Advanced Reports
* Advanced Collaboration
* Other additional optimization features

---

# 🖥️ Planned UI/UX Screens

The UI/UX will be designed in Figma before development.

## 1. 🔐 Authentication Screen

The Authentication section will include:

* Login
* Registration
* Email
* Password
* Confirm Password
* User Role

---

## 2. 📊 Main Dashboard

The Dashboard will contain:

* Sidebar Navigation
* Project Statistics
* Task Statistics
* Recent Projects
* Recent Tasks

---

## 3. 📄 Project / Task Details

The details view will display:

* Project Information
* Task Information
* Assignee
* Priority
* Status
* Due Date
* Description

---

## 4. 🗂️ Kanban Board

An additional screen will be designed for the Kanban workflow:

```text
TODO → IN PROGRESS → IN REVIEW → DONE
```

### Figma Design

**Coming Soon**

---

# 🗄️ Database Architecture

The application will use MongoDB for storing application data.

## Planned Collections

* Users
* Projects
* Tasks
* Comments

### Basic Relationship

```text
                USER
               /    \
              /      \
             ↓        ↓
        PROJECT      TASK
           │          │
           │          │
           └────→ TASK
                    │
                    ↓
                 COMMENTS
```

A detailed Entity Relationship Diagram (ERD) will be created during the system architecture phase.

---

# ⚛️ Frontend State Architecture

Redux Toolkit will be used for managing global application state.

## Planned Redux Store

```text
Redux Store
│
├── authSlice
│   ├── user
│   └── authentication state
│
├── projectSlice
│   ├── projects
│   └── selectedProject
│
├── taskSlice
│   ├── tasks
│   ├── selectedTask
│   └── filters
│
└── uiSlice
    ├── theme
    └── UI state
```

The complete State Tree Diagram will be created during the architecture phase.

---

# 🔌 Planned API Endpoints

## Authentication

```text
POST /api/auth/register
POST /api/auth/login
POST /api/auth/logout
```

## Projects

```text
GET    /api/projects
POST   /api/projects
GET    /api/projects/:id
PUT    /api/projects/:id
DELETE /api/projects/:id
```

## Tasks

```text
GET    /api/tasks
POST   /api/tasks
GET    /api/tasks/:id
PUT    /api/tasks/:id
DELETE /api/tasks/:id
```

These endpoints represent the planned API architecture and will be implemented progressively during development.

---

# 🏗️ System Architecture

The system architecture phase will include:

### Backend / Database

* MongoDB Collections
* Data Relationships
* Entity Relationship Diagram

### Frontend

* Redux State Tree
* Component Structure
* State Management Flow

### API

* Authentication Endpoints
* Project Endpoints
* Task Endpoints

### Architecture Diagram

**Coming Soon**

---

# 🎨 UI/UX Design

The application interface will be designed in Figma before implementation.

### Planned Designs

* Authentication / Registration
* Dashboard
* Project & Task Details
* Kanban Board

### Figma File

**Coming Soon**

---

# 📅 Development Plan

The project will be developed in multiple phases.

## Phase 1 — Foundation

* Project setup
* Authentication
* Registration
* Login / Logout
* Dashboard
* Basic application layout

## Phase 2 — Core Management

* Project CRUD
* Task CRUD
* Task Assignment
* Task Status Management

## Phase 3 — Selected P1 Features

* Kanban Board
* Search
* Filters

## Phase 4 — Testing & Deployment

* Unit Testing
* Component Testing
* Bug Fixes
* UI Refinement
* Production Build
* GitHub
* Vercel Deployment

---

# 📌 Project Scope

| Priority | Feature            | Status       |
| -------- | ------------------ | ------------ |
| P0       | Registration       | Planned      |
| P0       | Login / Logout     | Planned      |
| P0       | User Roles         | Planned      |
| P0       | Dashboard          | Planned      |
| P0       | Project CRUD       | Planned      |
| P0       | Task CRUD          | Planned      |
| P0       | Task Assignment    | Planned      |
| P0       | Task Status        | Planned      |
| P1       | Kanban Board       | Planned      |
| P1       | Search & Filters   | Planned      |
| P2       | Notifications      | Out of Scope |
| P2       | Advanced Analytics | Out of Scope |
| P2       | Advanced Reports   | Out of Scope |

---

# 📈 Project Status

**Current Status: Planning & Architecture Phase**

The project is currently in the Product Planning, UI/UX Design, and System Architecture stage.

Development will begin after the initial project blueprint and designs are finalized.

---

# 👩‍💻 Project Information

**Project Name:** TaskMatrix
**Project Type:** Agile Project Management Platform
**Designated Track:** Track A — Frontend Specialists
**Scope:** P0 + Selected P1 Features
**Development Status:** Planning Phase
