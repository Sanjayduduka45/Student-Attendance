# Student Attendance Management System

A lightweight, browser-based college attendance management app built with HTML, CSS, and vanilla JavaScript. The complete application is contained in `index.html`; no backend, build step, package installation, or external libraries are required.

## Run the application

Open `index.html` directly in a modern web browser. The app stores its data in that browser's `localStorage`, so changes persist between visits in the same browser.

## Demo sign-in

Choose a role on the login screen and use the matching credentials:

| Role | Email | Password |
|---|---|---|
| Admin | `admin@campus.edu` | `admin123` |
| Teacher | `emma@campus.edu` | `teach123` |
| Student | `aarav@campus.edu` | `student123` |

These are demo credentials, not secure authentication. The app is designed for local demonstration and does not provide server-side accounts, access control, or shared data across browsers.

## Features

### Admin

- View student, teacher, subject, attendance, and low-attendance statistics.
- Add, edit, search, filter, and delete student records.
- Add, edit, and delete teachers, including their subject and class assignments.
- Add, edit, and delete subjects and their department and class details.
- Review daily, weekly, monthly, student-wise, and subject-wise attendance reports.
- Export report rows to CSV.

### Teacher

- View assigned subjects, classes, student counts, and attendance activity.
- Select an assigned class, subject, and date to take attendance.
- Search the class roster, mark students present or absent, or mark the whole class at once.
- Review the session summary and save or edit attendance.
- Cancel and restore sessions; cancelled sessions are excluded from attendance calculations.
- Review saved attendance history.

### Student

- View overall and subject-wise attendance, total classes, presents, and absences.
- Check daily attendance status in the monthly calendar and attendance history.
- Read-only access to the attendance records.

## Attendance calculation

Attendance percentage is calculated as:

```text
(present classes / conducted classes) × 100
```

Future sessions and cancelled sessions are excluded. Students with no recorded classes have 0% attendance. Attendance status colors use green for 75% and above, yellow for 65–74%, and red for below 65%.

## Data and privacy

Data is stored locally in the browser's `localStorage`. It is not sent to a server and is not synchronized between devices or browsers. Clearing browser storage removes saved app data. Do not use the demo credentials or this local-only app to protect sensitive production data.
