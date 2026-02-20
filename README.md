# FlaskAuthApp

A Flask web application with user authentication and registration system.

## Features

- User registration with validation
- User login and session management
- Dashboard for authenticated users
- Password hashing for security
- SQLite database for user storage

## Fixed Issues

### Registration Validation Bug Fix
- ✅ **Name validation**: Name field cannot be empty
- ✅ **Email validation**: Email field cannot be empty and must be unique
- ✅ **Password validation**: Password field cannot be empty and must be at least 6 characters
- ✅ **Error handling**: Proper error messages displayed for validation failures
- ✅ **Server-side validation**: Backend validation implemented to prevent empty form submissions

## Installation

1. Clone the repository:
```bash
git clone https://github.com/prakharsingh070/flaskauth_app.git
cd flaskauth_app
```

2. Create a virtual environment:
```bash
python -m venv .venv
.venv\Scripts\activate  # On Windows
# source .venv/bin/activate  # On macOS/Linux
```

3. Install required packages:
```bash
pip install Flask Flask-SQLAlchemy Werkzeug
```

## Running the Application

1. Run the Flask application:
```bash
python app.py
```

2. Open your browser and navigate to `http://localhost:5000`

## Project Structure

```
FlaskAuthApp/
├── app.py              # Main application file
├── instance/
│   └── database.db     # SQLite database
├── templates/
│   ├── base.html       # Base template
│   ├── index.html      # Home page
│   ├── login.html      # Login page
│   ├── register.html   # Registration page
│   └── dashboard.html  # User dashboard
└── README.md           # Project documentation
```

## Routes

- `/` - Home page
- `/login` - User login
- `/register` - User registration (with validation)
- `/dashboard` - Protected user dashboard
- `/logout` - User logout

## Technologies Used

- **Backend**: Flask, SQLAlchemy
- **Frontend**: HTML, CSS (Bootstrap)
- **Database**: SQLite
- **Security**: Werkzeug password hashing

## Assignment Completion

This project addresses the registration validation bug where forms were being submitted successfully even with empty fields. The fix includes:

1. **Backend Validation**: Server-side validation in the `/register` route
2. **Error Handling**: Proper error messages for validation failures
3. **Form Security**: Prevention of empty field submissions
4. **User Experience**: Clear feedback for validation errors

## Deployment

The application is ready for deployment on platforms like Render, Heroku, or similar cloud services.