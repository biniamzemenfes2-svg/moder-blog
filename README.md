# moder-blog

# 📝 Personal Blog Website

A dynamic and responsive blog web application built with **Python and Flask**. The application allows users to create, read, edit, and delete blog posts through a clean and user-friendly interface.

This project demonstrates practical skills in Flask web development, database management, form validation, and CRUD operations.

## 🚀 Features

- **Create Blog Posts:** Publish articles with a title, subtitle, author, image URL, and body content.
- **View All Posts:** Display published articles on the homepage.
- **Read Individual Posts:** Open and read the full content of a blog post.
- **Edit Posts:** Update existing blog articles.
- **Delete Posts:** Remove unwanted blog posts.
- **Rich-Text Editing:** Write and format articles using CKEditor.
- **Form Validation:** Validate required fields and image URLs.
- **Responsive Design:** Use Bootstrap 5 for a mobile-friendly interface.
- **Database Storage:** Store blog posts using SQLite and Flask-SQLAlchemy.

## 🛠️ Technologies Used

| Technology        | Purpose                        |
| ----------------- | ------------------------------ |
| Python            | Backend programming            |
| Flask             | Web application framework      |
| Flask-SQLAlchemy  | Database integration and ORM   |
| SQLite            | Database storage               |
| Flask-WTF         | Form handling and validation   |
| Flask-Bootstrap 5 | Responsive UI components       |
| CKEditor          | Rich-text content editing      |
| HTML5 and CSS3    | Web page structure and styling |

## 📂 Project Structure

```text
blog-capstone/
├── main.py
├── requirements.txt
├── instance/
│   └── posts.db
├── static/
│   └── assets/
│       └── img/
└── templates/
    ├── index.html
    ├── post.html
    ├── make-post.html
    ├── about.html
    ├── contact.html
    ├── header.html
    └── footer.html
```

_Note: The exact database location and file structure may differ depending on your configuration._

## ⚙️ Installation and Setup

### 1. Clone the repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
cd YOUR_PROJECT_FOLDER
```

Replace the placeholder URL and folder name with your actual repository details.

### 2. Create a virtual environment

```bash
python3 -m venv .venv
```

Activate it on macOS or Linux:

```bash
source .venv/bin/activate
```

On Windows:

```bash
.venv\Scripts\activate
```

### 3. Install dependencies

If you have a `requirements.txt` file:

```bash
python -m pip install -r requirements.txt
```

Otherwise, install the main packages:

```bash
python -m pip install Flask bootstrap-flask Flask-SQLAlchemy Flask-WTF Flask-CKEditor
```

### 4. Run the application

```bash
python main.py
```

Open your browser and visit:

http://127.0.0.1:5003

## 🗄️ Database Model

The application uses a `BlogPost` model with the following fields:

| Field      | Description                   |
| ---------- | ----------------------------- |
| `id`       | Unique post identifier        |
| `title`    | Blog post title               |
| `subtitle` | Short description of the post |
| `author`   | Name of the author            |
| `date`     | Publication date              |
| `body`     | Main article content          |
| `img_url`  | URL of the post's image       |

The database tables are created automatically when the application starts.

## 🔄 Application Routes

| Route                    | Method    | Description              |
| ------------------------ | --------- | ------------------------ |
| `/`                      | GET       | Display all blog posts   |
| `/post/<post_id>`        | GET       | View an individual post  |
| `/new_post`              | GET, POST | Create a new post        |
| `/edit_post/<post_id>`   | GET, POST | Edit an existing post    |
| `/delete_post/<post_id>` | POST      | Delete a post            |
| `/about`                 | GET       | Display the About page   |
| `/contact`               | GET       | Display the Contact page |

## 📚 What I Learned

Building this project helped me practice:

- Developing web applications with Flask.
- Defining database models using SQLAlchemy.
- Implementing create, read, update, and delete operations.
- Handling and validating forms with Flask-WTF.
- Integrating a rich-text editor.
- Using Jinja2 templates and template inheritance.
- Building responsive pages with Bootstrap 5.
- Managing routes and HTTP methods.

## 🔐 Security Notes

- Keep your Flask secret key private and use an environment variable in production.
- Protect form submissions with CSRF validation.
- Sanitize rich-text HTML before rendering user-submitted content.
- Use POST requests for destructive actions such as deleting posts.
- Add authentication and authorization before allowing multiple users to manage posts.

## 🌱 Future Improvements

- User registration and login.
- Categories and tags for blog posts.
- Search and pagination.
- Comments and likes.
- Image uploads.
- Deployment to a production hosting platform.

## 👨‍💻 Author

**Biniam Zemenfes**

Software Engineering Student | Python & Flask Developer

---

_Built as a hands-on project to strengthen my backend and full-stack web development skills._
