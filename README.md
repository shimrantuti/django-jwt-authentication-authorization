# Django JWT Authentication & Authorization System

A backend authentication and authorization system built with Django and Django REST Framework.

This project is being developed step by step to understand how authentication, JWT tokens, custom user models, and authorization work in a real-world backend application.

## 🎯 Project Goal

The goal of this project is to build an authentication system that includes:

- Custom user model with email-based login.
- User registration API.
- JWT-based authentication.
- Access and refresh tokens.
- Protected API endpoints.
- Role-based authorization.
- Custom permissions.
- Frontend integration support.

## 🛠️ Technology Stack

- **Programming Language:** Python
- **Backend Framework:** Django
- **API Framework:** Django REST Framework
- **Authentication:** JSON Web Tokens (JWT)
- **JWT Library:** djangorestframework-simplejwt
- **CORS Handling:** django-cors-headers
- **Database:** SQLite (development)

---

## 🚀 Project Setup & Development Journey

This section documents how I created and configured the project from scratch.

### 1. Create a Virtual Environment

A virtual environment keeps project dependencies separate from other Python projects.

Create the environment:

```bash
python -m venv .venv

```

Activate it on Windows PowerShell:

```powershell
.venv\Scripts\Activate.ps1

```

After activation, the terminal displays `(.venv)`.

### 2. Install Django

Install Django using pip:

```bash
pip install django

```

Verify the installation:

```bash
django-admin --version

```

### 3. Create the Django Project

Create the Django project:

```bash
django-admin startproject jwtauthapi

```

Move into the project directory:

```bash
cd jwtauthapi

```

> The Django project package is named `jwtauthapi`. The GitHub repository has a separate name.

### 4. Create the Account Application

Create an application to manage users and authentication:

```bash
python manage.py startapp account

```

The `account` app will contain the user model, user manager, serializers, views, and authentication-related logic.

### 5. Install Django REST Framework

Django REST Framework is used to build APIs.

```bash
pip install djangorestframework

```

Add it to `INSTALLED_APPS` in `settings.py`:

```python
INSTALLED_APPS = [
    # ...
    "rest_framework",
    "account",
]

```

### 6. Install JWT Authentication

I referred to the official documentation of **Django REST Framework Simple JWT** to understand token-based authentication.

Install the package:

```bash
pip install djangorestframework-simplejwt

```

Simple JWT provides built-in views for obtaining and refreshing JWT tokens.

The commonly used views include:

- `TokenObtainPairView`
- `TokenRefreshView`

These views can be used to implement a standard JWT login and token-refresh flow.

### 7. Explore Manual JWT Token Creation

In addition to using built-in JWT views, I studied how JWT tokens can be created manually using the Simple JWT library.

This helps me understand:

- How access tokens are generated.
- How refresh tokens are generated.
- How user information is associated with tokens.
- How token expiration works.
- How authentication can be customized.

Manual token creation will be implemented and documented as the project develops.

### 8. Install CORS Headers

To support communication between a frontend application and the Django backend, I installed `django-cors-headers`.

```bash
pip install django-cors-headers

```

CORS configuration helps manage which frontend origins are allowed to communicate with the backend.

The configuration will be documented once the frontend integration is implemented.

### 9. Study Django Custom Authentication

To create a custom user model, I referred to Django's official documentation on customizing authentication.

The custom user system is being designed with:

- Email-based login.
- A custom `UserManager`.
- Password hashing using Django's password utilities.
- Custom user fields.
- Admin and staff access handling.

The implementation is being developed incrementally and will be documented with the relevant code and design decisions.

---

## 📁 Project Structure

```text
jwtauthapi/
│
├── account/
│   ├── migrations/
│   ├── admin.py
│   ├── apps.py
│   ├── models.py
│   ├── tests.py
│   └── views.py
│
├── jwtauthapi/
│   ├── settings.py
│   ├── urls.py
│   ├── asgi.py
│   └── wsgi.py
│
├── manage.py
├── .gitignore
└── README.md

```

## 🔐 Planned Authentication Flow

```text
User Registration
       ↓
Custom User Model
       ↓
JWT Login
       ↓
Access and Refresh Tokens
       ↓
Protected API Requests
       ↓
Permission Checking
       ↓
Allow or Deny Access

```

## 🚧 Development Progress

### Completed

-  Django project setup.
-  `account` application created.
-  Virtual environment configured.
-  Django REST Framework installed.
-  Simple JWT package installed.
-  CORS headers package installed.
-  Git and GitHub repository setup.

### In Progress / Upcoming

-  Custom User Model.
-  Custom User Manager.
-  User Registration API.
-  JWT Login.
-  Manual token creation.
-  Access and refresh token handling.
-  Protected API endpoints.
-  Role-based authorization.
-  Custom permissions.
-  API testing.
-  Frontend integration.

## 📌 Planned API Endpoints

| MethodEndpointPurpose |                   |                         |
| --------------------- | ----------------- | ----------------------- |
| POST                  | `/register/`      | Register a new user     |
| POST                  | `/login/`         | Authenticate a user     |
| POST                  | `/token/refresh/` | Refresh an access token |
| GET                   | `/profile/`       | View user profile       |
| PUT                   | `/profile/`       | Update user profile     |

> These endpoints will be implemented and documented as the project progresses.

## 📚 Learning Resources

- [Django Documentation — Customizing Authentication](https://docs.djangoproject.com/en/stable/topics/auth/customizing/)
- [Django REST Framework Documentation](https://www.django-rest-framework.org/)
- [Simple JWT Documentation](https://django-rest-framework-simplejwt.readthedocs.io/)
- [django-cors-headers Documentation](https://github.com/adamchainz/django-cors-headers)

## 🔮 Future Improvements

- Password reset.
- Email verification.
- More granular permissions.
- Automated tests.
- PostgreSQL support.
- API documentation.
- Production deployment.

## 👩‍💻 Developer

**Shimran Tuti**

GitHub: [shimrantuti](https://github.com/shimrantuti)  