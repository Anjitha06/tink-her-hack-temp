<p align="center">
  <img src="./img.png" alt="Project Banner" width="100%">
</p>

# Campus Care 🎯

## Basic Details

### Team Name: Pixels

### Team Members
- Member 1: Anjitha Aravind - College of Engineering Chengannur
- Member 2: Devananda P Nair- College of Engineering Chengannur

### Hosted Project Link
https://campus-care-frontend.vercel.app/

### Project Description
CampusCare Portal is a centralized campus management platform that bridges communication between students and administration. It enables students to raise complaints, track resolutions, vote on important issues, and monitor cleaning and maintenance activities — all within a unified system.

The platform promotes transparency, accountability, and structured issue resolution through real-time updates, intelligent status tracking, and systematic maintenance scheduling.

### The Problem statement
Educational institutions often face challenges in efficiently managing campus cleaning and maintenance activities. Many schedules are manually recorded, poorly tracked, or inconsistently monitored, leading to delays, missed tasks, and operational inefficiencies.

Additionally, the absence of a centralized system makes it difficult to ensure transparency, track task completion, and maintain accountability.

On top of that, communication gaps in complaint resolution and issue prioritization further reduce the effectiveness of campus management systems.

### The Solution
CampusCare Portal is designed primarily as a structured schedule management and tracking platform for campus cleaning and maintenance activities. It enables administrators to create, monitor, and manage schedules with intelligent status updates (Scheduled / In Progress / Completed) based on real-time date logic.

In addition to schedule monitoring, the platform integrates:
	•	A complaint reporting and tracking module
	•	A voting mechanism to prioritize reported issues
	•	Role-based dashboards for Admin and Users
	•	Real-time notifications for status updates and responses

By combining automated schedule tracking with structured issue management, the system ensures transparency, operational efficiency, and continuous campus improvement.

---

## Technical Details

### Technologies/Components Used

**For Software:**
- Languages used: JavaScript
- Frameworks used: Node.js,Express.js
- Libraries used: Mongoose,JWT (Authentication)
- Tools used: VS Code – Development environment
              Git – Version control
              GitHub – Repository hosting & collaboration
              Thunder Client (VS Code Extension) – API testing
              Vercel – Frontend deployment and hosting platform

---

## Features

List the key features of your project:
- Campus Cleaning Schedule Management: Administrators can create, update, and manage cleaning schedules for different campus areas. Students can view upcoming, ongoing, and completed cleaning activities in real time.

- Maintenance & Complaint Registration System: Students can register maintenance complaints related to campus facilities such as hostels, classrooms, or common areas. Each complaint includes details like area, description, and submission timestamp.

- Community Voting & Issue Prioritization: Students can vote on complaints to highlight urgent or commonly faced issues. This ensures high-impact problems are prioritized by the administration.

- Real-Time Status Tracking:  Each complaint and schedule includes dynamic status updates (Scheduled, In Progress, Completed, Resolved). Users can track progress transparently without needing manual follow-ups.

-Role-Based Authentication System: Separate login systems for Admin and Users ensure secure access control. Admins can manage schedules and respond to complaints, while users can submit and track issues.

-Notification System: Users receive update notifications when their complaints are responded to or resolved, improving communication transparency.



---

## Implementation

### For Software:

#### Installation
```bash
npm install
```

#### Run
```bash
 npm start
```

---

## Project Documentation

### For Software:

#### Screenshots (Add at least 3)

![thh login page](https://github.com/user-attachments/assets/8e5f4a74-feb3-4015-b537-c449c12d46a8)
*Portal face*

![separatelogin](https://github.com/user-attachments/assets/061bc82a-32ac-49af-9fa3-7c38daf051f6)
*Login Interface for admin and user*

![issue_impact_view_on_admin](https://github.com/user-attachments/assets/a7c23597-7308-4087-b473-03913f1546aa)
*Prioritising complanits based on statistical comparisons*




#### Build Photos


<img width="1024" height="1024" alt="pixels" src="https://github.com/user-attachments/assets/1b62ccf1-2bdb-4779-88e8-dd5ec845987b" />

![thh login page](https://github.com/user-attachments/assets/5fca0069-6550-4d8c-9619-3f06036ec996)

*Campus Care*

---

---

## Additional Documentation

---

# For Web Projects with Backend

## API Documentation

**Base URL:**  
```https://campus-care-frontend.vercel.app/ 
```

---

### POST /api/auth/login

**Description:** Authenticates a student or admin user and returns a JWT token.

**Request Body:**
```json
{
  "email": "student@college.edu",
  "password": "password123",
  "role": "student"
}
```

**Response:**
```json
{
  "status": "success",
  "token": "jwt_token_here",
  "user": {
    "id": "u123",
    "name": "Anjitha",
    "role": "student"
  }
}
```

---

### POST /api/complaints

**Description:** Allows students to submit a cleaning or maintenance complaint.

**Request Body:**
```json
{
  "location": "Block A - 2nd Floor",
  "category": "Cleaning",
  "description": "Dust accumulation near staircase",
  "priority": "medium"
}
```

**Response:**
```json
{
  "status": "success",
  "message": "Complaint submitted successfully",
  "complaintId": "c101"
}
```

---

### GET /api/complaints

**Description:** Fetches complaints. Admin can view all complaints. Students can view their own complaints.

**Query Parameters:**
- `status` (pending / in-progress / resolved)
- `category` (Cleaning / Maintenance)

**Response:**
```json
{
  "status": "success",
  "data": [
    {
      "id": "c101",
      "location": "Library",
      "category": "Maintenance",
      "description": "Broken light",
      "status": "pending",
      "createdAt": "2026-02-28T10:30:00Z"
    }
  ]
}
```

---

### PUT /api/complaints/:id

**Description:** Updates the status of a complaint (Admin only).

**Request Body:**
```json
{
  "status": "resolved"
}
```

**Response:**
```json
{
  "status": "success",
  "message": "Complaint status updated successfully"
}
```

---

### DELETE /api/complaints/:id

**Description:** Deletes a complaint (Admin only).

**Response:**
```json
{
  "status": "success",
  "message": "Complaint deleted successfully"
}
```

---

# System Architecture

Frontend:
- Built using HTML, CSS, and JavaScript
- Role-based UI rendering (Student / Admin dashboards)

Backend:
- Node.js with Express.js
- RESTful API structure
- JWT-based authentication

Database:
- MongoDB for storing users and complaints
- Separate collections for users and complaint records

Deployment:
- Frontend deployed using Vercel
- Backend hosted on Vercel serverless functions
- Version control using Git and GitHub

---

# Project Demo

Video Link: https://drive.google.com/file/d/1zdh3-huKLYzQtagubgUaKtLB9G3ekvnj/view?usp=sharing

The demo demonstrates:
- Student login and dashboard access
- Complaint submission process
- Admin dashboard overview
- Complaint filtering and status update
- Real-time complaint tracking

Live Website: https://campus-care-frontend.vercel.app/ 
GitHub Repository: https://github.com/Devananda-jpg/CampusCare/tree/main

---

# AI Tools Used (For Transparency)

Tool Used: ChatGPT

Purpose:
- API design suggestions
- Debugging backend logic
- Structuring authentication flow
- Documentation formatting assistance

Approximate AI-generated code: 20%

Human Contributions:
- Complete system architecture design
- Role-based access control implementation
- Database schema design
- UI design and layout decisions
- Testing and deployment configuration

---

# Team Contributions

Anjitha Aravind – Frontend development, API integration, documentation, deployment  
Devananda P Nair  – Backend development, authentication logic, database management   

---

# License

This project is licensed under the MIT License.

---

Made with ❤️ at TinkerHub
