# Mergington High School Activities

A website application that allows students to view and sign up for extracurricular activities at Mergington High School.

## Features

- View all available extracurricular activities
- Filter activities by category (Sports, Arts, Academic, Community, Technology)
- Filter activities by day of the week
- Filter activities by time (Before School, After School, Weekend)
- Filter activities by difficulty level (Beginner, Intermediate, Advanced)
- Search activities by name
- Sign up students for activities (requires teacher login)
- Unregister students from activities (requires teacher login)
- Teacher login and logout
- Dark mode toggle

## API Endpoints

| Method | Endpoint | Description |
| ------ | -------- | ----------- |
| GET | `/activities` | Get all activities, with optional `day`, `start_time`, and `end_time` filters |
| GET | `/activities/days` | Get a list of all days that have activities scheduled |
| POST | `/activities/{activity_name}/signup?email={student_email}&teacher_username={username}` | Sign up a student for an activity (requires teacher authentication) |
| POST | `/activities/{activity_name}/unregister?email={student_email}&teacher_username={username}` | Remove a student from an activity (requires teacher authentication) |
| POST | `/auth/login` | Log in as a teacher (pass `username` and `password` as query parameters) |
| GET | `/auth/check-session?username={username}` | Check if a teacher session is valid |

## Development Guide

For detailed setup and development instructions, please refer to our [Development Guide](../docs/how-to-develop.md).
