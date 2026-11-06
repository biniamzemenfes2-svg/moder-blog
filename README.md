# PERSONAL Blog Website

A dynamic blog website built with **Python and Flask**, allowing users to register, log in, read blog posts, and leave comments. The website also provides administrative functionality for creating, editing, and managing blog posts.

## Features

- **User Authentication**
  - User registration and login.
  - Secure password hashing.
  - User logout and session management.

- **Blog Management**
  - Display all published blog posts.
  - View individual blog posts.
  - Create new blog posts.
  - Edit existing posts.
  - Restrict post management to the administrator.

- **Comment System**
  - Authenticated users can leave comments.
  - Display comments under individual blog posts.
  - Associate comments with their authors and blog posts.

- **User Interface**
  - Responsive design using Bootstrap 5.
  - Rich-text editing with Flask-CKEditor.
  - Profile images using Flask-Gravatar.

## Technologies Used

| Technology       | Purpose                      |
| ---------------- | ---------------------------- |
| Python           | Backend programming          |
| Flask            | Web framework                |
| Flask-SQLAlchemy | Database management          |
| SQLite           | Database                     |
| Flask-Login      | User authentication          |
| Flask-WTF        | Form handling and validation |
| Flask-Bootstrap5 | Responsive styling           |
| Flask-CKEditor   | Rich-text editing            |
| Werkzeug         | Password hashing             |
| Jinja2           | HTML templating              |

## Project Structure

```text
blog-website/
│
├── app.py
├── forms.py
├── requirements.txt
│
├── templates/
│   ├── index.html
│   ├── post.html
│   ├── login.html
│   ├── register.html
│   ├── make-post.html
│   ├── header.html
│   └── footer.html
│
├── static/
│   ├── assets/
│   ├── css/
│   ├── js/
│   └── img/
│
└── instance/
    └── posts.db
```

_The structure above is illustrative. Adjust filenames and folders to match your actual project._

## Installation and Setup

### 1. Clone the Repository

```bash
git clone YOUR_REPOSITORY_URL
cd YOUR_PROJECT_FOLDER
```

### 2. Create a Virtual Environment

```bash
python3 -m venv .venv
```

Activate it:

**macOS / Linux**

```bash
source .venv/bin/activate
```

**Windows**

```bash
.venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure the Application

Set your Flask secret key in the application configuration. For a real deployment, use an environment variable rather than committing secrets to GitHub.

### 5. Initialize the Database

If your application uses `db.create_all()`, initialize the database within the Flask application context:

```python
with app.app_context():
    db.create_all()
```

### 6. Run the Application

```bash
python app.py
```

Open your browser and visit:

```text
http://127.0.0.1:5000/
```

## Database Models

The application uses SQLAlchemy models to manage its data.

- **User:** Stores registered users and their authentication information.
- **BlogPost:** Stores blog post information, including title, subtitle, body, image URL, and author.
- **Comment:** Stores comments associated with users and blog posts.

The models use SQLAlchemy relationships to connect users, posts, and comments.

## Security

- Passwords are stored as secure hashes rather than plain text.
- Flask-Login manages authenticated user sessions.
- Administrative routes are protected from unauthorized access.
- Flask-WTF supports form validation and CSRF protection.

## Future Improvements

- User profile management.
- Search and filter blog posts.
- Pagination for blog posts.
- Categories and tags.
- Improved comment moderation.
- Deployment to a production hosting platform.

## Author

Developed as part of my journey in learning **Python, Flask, SQLAlchemy, and full-stack web development**.

---

⭐ If you find this project useful, consider giving the repository a star!
