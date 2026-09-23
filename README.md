# Health-Activity-Tracker

A full-stack personal health activity tracking application that allows users to record daily activities, set personal goals, monitor progress, analyze activity trends, and view historical summaries through a responsive dashboard.

Project Overview
The system helps users maintain a structured record of their daily physical activities such as walking, running, cycling, and exercise. Users can define personal activity goals and compare their actual performance against their targets.
The application provides **history tracking, progress monitoring, trend charts, analytics, and activity summaries** to help users understand their activity patterns over time.

Key Features

User registration and login
Personalized dashboard
Add daily activities
Edit incorrect activity records
Delete activity records
Create and manage personal goals
Track progress toward goals
View daily and historical activity records
Filter activities by date and activity type
View daily, weekly, and monthly activity trends
Interactive activity charts and analytics
Activity streak tracking
Personal achievements and best records
Activity-based smart insights
Generate activity summaries and reports
Export activity data
Responsive design for desktop, tablet, and mobile
Persistent database storage

## Application Workflow

User Registration / Login
          ↓
      Dashboard
          ↓
 ┌────────┼─────────┐
 ↓        ↓         ↓
Activities Goals   History
 ↓        ↓         ↓
Add/Edit  Set      Filter
Activity  Target   Records
 └────────┼─────────┘
          ↓
    Progress Engine
          ↓
  Actual vs Goal
          ↓
     Progress %
          ↓
   Analytics & Trends
          ↓
   Reports & Insights
          ↓
       Database

## Main Modules

### 1. Authentication
Users can securely register, log in, and manage their account.

### 2. Dashboard
Provides an overview of:

* Today's activities
* Goal progress
* Activity statistics
* Recent records
* Weekly trends

### 3. Activity Management
Users can:
* Add activities
* Edit activities
* Delete activities
* View activity details

Supported activities may include:
* Walking
* Running
* Cycling
* Exercise
* Other supported activities

### 4. Goal Management
Users can create personal activity goals by defining:

* Activity type
* Target value
* Unit
* Frequency
* Start date
* End date

### 5. History
Users can review previous activity records and filter them by:

* Date
* Date range
* Activity type
* Daily/weekly/monthly period

### 6. Analytics & Trends
The system visualizes stored activity data using charts such as:

* Weekly activity trends
* Monthly activity trends
* Activity comparisons
* Goal completion
* Activity distribution

### 7. Progress Engine
The system compares recorded activity with the selected goal.
Progress % = (Actual Activity / Goal Target) × 100
Example:

Actual = 6,240 steps
Goal   = 8,000 steps

Progress = 78%

### 8. Summaries & Reports
Users can view:
* Daily summaries
* Weekly summaries
* Monthly summaries
* Total activity duration
* Average activity
* Goal completion

## Technology Stack
### Frontend
* React.js
* JavaScript
* HTML5
* CSS3
* Responsive UI
* Charting library

### Backend
* Node.js
* Express.js
* REST APIs

### Database
* Supabase / PostgreSQL

### Development Tools
* Visual Studio Code
* Git
* GitHub
* npm

## Database Structure
The application stores data using relational database tables.

Users
  │
  ├── Activities
  │
  ├── Goals
  │
  └── Reminders

### Main Tables

**Users**
* User ID
* Name
* Email
* Password
* Created At

**Activities**
* Activity ID
* User ID
* Activity Type
* Activity Date
* Quantity
* Unit
* Duration
* Notes
* Created At
* Updated At

**Goals**
* Goal ID
* User ID
* Activity Type
* Target Value
* Unit
* Frequency
* Start Date
* End Date

## Project Structure


health-activity-tracker/
│
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── services/
│   │   ├── utils/
│   │   ├── App.jsx
│   │   └── main.jsx
│   ├── package.json
│   └── ...
│
├── backend/
│   ├── src/
│   │   ├── controllers/
│   │   ├── routes/
│   │   ├── models/
│   │   ├── services/
│   │   ├── middleware/
│   │   └── config/
│   ├── server.js
│   ├── package.json
│   └── .env
│
├── database/
│   └── schema.sql
│
├── README.md
└── .gitignore

Installation & Setup
1. Clone the repository
git clone https://github.com/your-username/health-activity-tracker.git

2. Navigate to the project
cd health-activity-tracker

3. Install frontend dependencies
cd frontend
npm install

4. Install backend dependencies
cd ../backend
npm install

5. Configure environment variables
Create a `.env` file inside the backend directory.
PORT=5000
DATABASE_URL=your_database_url
Add any required frontend environment variables in the frontend `.env` file.

6. Start the backend
npm run dev

7. Start the frontend
cd frontend
npm run dev

The application will then be available through the local development URL shown by Vite.

## Responsive Design
The application is designed to work across:
* 💻 Desktop
* 📱 Mobile
* 📲 Tablet
The dashboard, activity cards, forms, tables, navigation, and charts adapt to different screen sizes.

## Security

The application follows basic security practices such as:
* Environment variables for sensitive configuration
* Authentication
* Input validation
* Protected API operations
* Database access control
* `.env` excluded from Git using `.gitignore`


## 💡 Future Enhancements

* Wearable device integration
* Google Fit / Apple Health integration
* Push notifications
* Advanced personalized recommendations
* Offline support
* More activity types
* PDF report generation
* Advanced analytics
* Mobile application



This project is developed for educational and hackathon purposes.
