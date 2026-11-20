# FastAPI-Course-Management-Backend
This repository contains a high-performance backend API built using FastAPI. It is designed to handle core operations for an educational platform, including user registration, course management, enrollment, and analytics dashboards.   
## Features

- Public Health/Live Check: Quick validation endpoint to ensure the backend is running.
- Dashboard Analytics: Returns system-wide statistics for students, teachers, courses, and enrollments.
- User Registration: Processes registrations for students, teachers, or administrators.
- Course Management: Allows creation and publishing of new courses with difficulty levels.
- Course Enrollment: Enrolls students in specific courses.
- Teacher Analytics: Returns detailed student progress tracking.

## Tech Stack

- Framework: FastAPI
- Server: Uvicorn
- Tunneling: pyngrok
- Language: Python
- Helper Libraries: Pydantic (data validation), SQLAlchemy

## Prerequisites

Ensure you have Python installed, then install the required dependencies:

```bash
pip install fastapi uvicorn pyngrok pydantic nest-asyncio
```

## API Endpoints

### General
- `GET /` - Check backend live status
- `GET /admin-dashboard` - Retrieve high-level statistics
- `GET /teacher-analytics` - Retrieve student progress metrics

### Actions
- `POST /register` - Register a new user
  - Request Body: `name` (string), `email` (string), `role` (string)
- `POST /add-course` - Create a new course
  - Request Body: `title` (string), `category` (string), `difficulty` (string), `teacher` (string)
- `POST /enroll` - Enroll a student in a course
  - Request Body: `student_id` (integer), `course_id` (integer)

## How to Run

1. Save the backend code to a Python file, for example `main.py`.
2. In your code, replace the ngrok authentication token with your own token from your ngrok dashboard.
3. Run the application:

```bash
python main.py
```

4. Once running, copy the generated public URL printed in the terminal and update your frontend application with this base URL.
