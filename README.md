# TweetCom

TweetCom is a Django-based mini social media app inspired by Twitter/X. It allows users to register, log in, create tweets, upload images, and edit or delete their own posts.

## Features

- User registration and authentication
- Create, edit, and delete tweets
- Image upload support for tweets
- Responsive UI using Bootstrap
- SQLite database for local development
- Login/logout flow with Django auth

## Tech Stack

- Python 3.14+
- Django 6.1.1
- Pillow 12.3.0
- SQLite
- Bootstrap 5

## Project Structure

```text
DjangoApplication/
├── DjangoApp/
│   ├── DjangoApp/
│   │   ├── __init__.py
│   │   ├── settings.py
│   │   ├── urls.py
│   │   ├── asgi.py
│   │   └── wsgi.py
│   ├── templates/
│   │   ├── layout.html
│   │   └── registration/
│   ├── tweetcom/
│   │   ├── templates/
│   │   ├── admin.py
│   │   ├── forms.py
│   │   ├── models.py
│   │   ├── urls.py
│   │   ├── views.py
│   │   └── migrations/
│   ├── db.sqlite3
│   ├── manage.py
│   └── media/
├── requirements.txt
├── .venv/
└── README.md
```

## Prerequisites

- Python 3.10+
- pip
- Virtual environment support

## Setup

1. Clone the repository and navigate to the project root:

```bash
cd DjangoApplication
```

2. Create and activate a virtual environment:

```bash
python -m venv .venv
.venv\Scripts\activate
```

3. Install dependencies:

```bash
pip install -r requirements.txt
```

4. Apply migrations:

```bash
cd DjangoApp
python manage.py migrate
```

5. Create a superuser (optional but recommended for admin access):

```bash
python manage.py createsuperuser
```

## Run the Application

From the `DjangoApp` directory:

```bash
python manage.py runserver
```

Then open:

```text
http://127.0.0.1:8000/tweetcom/
```

Admin panel:

```text
http://127.0.0.1:8000/admin/
```

## Default Behavior

- Users can register from the application UI.
- Logged-in users can create new tweets with optional images.
- Only the owner of a tweet can edit or delete it.
- Uploaded media is stored under the `media/` folder.

## Notes

- This project is configured for local development and uses SQLite.
- `DEBUG` is currently enabled as default for development.
- The app includes a basic Bootstrap-based layout and templates for authentication and tweet management.

## License

This project is provided as a learning/demo application. Add a license file if you plan to distribute it publicly.
