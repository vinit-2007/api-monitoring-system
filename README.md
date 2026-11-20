API Monitoring System

LIVE LINK: https://api-monitoring-system.netlify.app/

A full-stack API Monitoring System built to monitor API endpoints on a scheduled basis, track uptime and response times, maintain execution logs, visualize performance metrics, and automatically send email alerts when API failures occur.

Features
API Management: Add, manage, and monitor API endpoints.
Dashboard: View overall API health, uptime status, and performance metrics.
Response Time Visualization: Analyze API response times through interactive charts.
Execution Logs: Maintain historical records of API checks, response times, and status codes.
Automated Monitoring: Execute scheduled API health checks using cron jobs.
Downtime Detection: Detect failed requests and unavailable API endpoints.
Email Notifications: Automatically send email alerts when monitored APIs encounter issues.
Alert Management: Track and manage alert states.
Responsive UI: User-friendly interface built with React and Tailwind CSS.
Tech Stack
Frontend
React.js
Vite
Tailwind CSS
Recharts
Backend
Node.js
Express.js
Node Cron
MVC Architecture
Modular Service Architecture
Database & Notifications
MongoDB
Mongoose
Nodemailer
Project Structure
text
api-monitoring-system/
│
├── backend/
│   ├── src/
│   │   ├── config/
│   │   ├── controllers/
│   │   ├── cron/
│   │   ├── middleware/
│   │   ├── models/
│   │   ├── routes/
│   │   ├── services/
│   │   └── utils/
│   │
│   ├── package.json
│   └── package-lock.json
│
└── frontend/
    ├── src/
    │   ├── api/
    │   ├── charts/
    │   ├── components/
    │   ├── layouts/
    │   ├── pages/
    │   └── main.jsx
    │
    ├── package.json
    └── vite.config.js

Installation & Setup
1. Clone the Repository
bash
git clone your_repository_url
cd api-monitoring-system

2. Backend Setup
bash
cd backend
npm install


Create a .env file inside the backend/ directory.

3. Environment Variables
env
# Server Configuration
PORT=5000

# Database Configuration
MONGO_URI=your_mongodb_uri

# Email Configuration
EMAIL_USER=your_email
EMAIL_PASS=your_email_app_password
ALERT_EMAIL=your_alert_receiver_email

# Frontend Configuration
CLIENT_URL=http://localhost:5173


Replace the placeholder values with your actual MongoDB connection string and email credentials.

4. Start the Backend
bash
npm install
npm run dev

5. Frontend Setup

Open a new terminal:

bash
cd frontend
npm install
npm run dev


The frontend will be available at:

text
http://localhost:5173

How It Works
Register API endpoints through the application.
The backend scheduler periodically executes health checks.
API responses, status codes, and response times are recorded.
Monitoring results are displayed on the dashboard.
Failed API checks trigger email notifications.
Historical execution logs help analyze API performance and downtime.
Project Highlights
Automated API health monitoring.
Scheduled background monitoring using cron jobs.
Centralized performance analytics dashboard.
Response time tracking and visualization.
Historical monitoring and execution logs.
Automated email-based incident notifications.
Modular and maintainable backend architecture.
Responsive React frontend.
Security
Keep database credentials and email passwords in environment variables.
Never commit .env files to version control.
Use .env.example to document required configuration variables without exposing secrets.
License

This project is intended for educational and development purposes.
