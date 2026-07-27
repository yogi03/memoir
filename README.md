# Memoir

Memoir is a Django-based blogging platform with user accounts and a rich-text post editor. It's built as a standard Django project with dedicated apps for blog content and user management.

## Features

- User registration and authentication (`users` app)
- Create, edit, and browse blog posts (`blog` app)
- Rich-text post editing via TinyMCE
- Styled forms using django-crispy-forms with the Bootstrap 5 template pack

## Tech Stack

- [Django](https://www.djangoproject.com/) 5.0.6
- [django-crispy-forms](https://django-crispy-forms.readthedocs.io/) + [crispy-bootstrap5](https://github.com/django-crispy-forms/crispy-bootstrap5)
- [django-tinymce](https://github.com/aljosa/django-tinymce) for WYSIWYG editing
- SQLite (default, via `db.sqlite3`)

## Project Structure

```
memoir/
├── app_blog/        # Django project (settings, root URLs, WSGI/ASGI)
├── blog/            # Blog app — posts, views, templates
├── users/           # User accounts app — registration, auth
├── db.sqlite3       # Default SQLite database
├── manage.py        # Django management script
├── Pipfile          # Pipenv dependency file
└── requirements.txt # Pip dependency list
```

## Getting Started

### Prerequisites

- Python 3.10+
- pip (or Pipenv, since a `Pipfile` is included)

### Installation

1. Clone the repository

   ```bash
   git clone https://github.com/yogi03/memoir.git
   cd memoir
   ```

2. Create and activate a virtual environment

   ```bash
   python -m venv venv
   source venv/bin/activate   # On Windows: venv\Scripts\activate
   ```

3. Install dependencies

   ```bash
   pip install -r requirements.txt
   ```

   Or, if you prefer Pipenv:

   ```bash
   pipenv install
   pipenv shell
   ```

4. Apply database migrations

   ```bash
   python manage.py migrate
   ```

5. Create a superuser (optional, for admin access)

   ```bash
   python manage.py createsuperuser
   ```

6. Run the development server

   ```bash
   python manage.py runserver
   ```

7. Open your browser at `http://127.0.0.1:8000/`

## Usage

- Register a new account or log in via the `users` app.
- Create and publish blog posts through the `blog` app, using the TinyMCE editor for formatted content.
- Visit `/admin/` (after creating a superuser) to manage posts and users from the Django admin site.

## Contributing

Contributions are welcome. Please open an issue to discuss any significant changes before submitting a pull request.

## License

No license has been specified for this project. Please contact the repository owner ([yogi03](https://github.com/yogi03)) for usage terms.
