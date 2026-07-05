# Library Management System

![Python](https://img.shields.io/badge/python-%233670A0.svg?style=for-the-badge&logo=python&logoColor=ffdd54)
![Django](https://img.shields.io/badge/django-%23092E20.svg?style=for-the-badge&logo=django&logoColor=white)
![React](https://img.shields.io/badge/react-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB)
![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)
![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/postgresql-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white)

A full-stack web application developed to manage library catalogs, users, and the complete flow of book lending and returns. The project features a robust RESTful API on the backend and a dynamic interface on the frontend.

## Features
* **Catalog Management**: Full administration of books and bibliographic documents.
* **Lending Control**: Precise tracking of checkouts, due dates, and returns.
* **User Administration**: Profile management with role-based access and JWT token authentication.
* **REST API**: Structured and secure endpoints for client-server communication.

## Stack
* **Backend**: `Python (Django)`, `Django REST Framework`, `Simple JWT`
* **Frontend**: `React`, `Vite`, `HTML5/CSS3/JavaScript`
* **Database**: `PostgreSQL`
* **Server Deployment**: `Gunicorn` & `Whitenoise`

## Prerequisites
Make sure you have the following installed in your local environment:
* [Python 3.10+](https://www.python.org/downloads/)
* [Node.js](https://nodejs.org/)
* [PostgreSQL](https://www.postgresql.org/)

## Getting Started

### Clone the repository

```bash
git clone https://github.com/fcabrerapd/sistema-biblioteca
cd sistema-biblioteca
```
### Setup Environment Variables
Create a .env file in the root of the backend directory and add your database and Django configuration:
```bash
SECRET_KEY=your_django_secret_key_here
DEBUG=True
DB_NAME=biblioteca_db
DB_USER=postgres
DB_PASSWORD=your_password
DB_HOST=localhost
DB_PORT=5432
```
### Run Backend (Django)
Open a terminal, navigate to the backend folder, and start the server:
```bash
cd backend
python -m venv .venv

# On Windows:
.venv\Scripts\activate
# On macOS/Linux:
# source .venv/bin/activate

pip install -r requirements.txt
python manage.py migrate
python manage.py runserver
```
### Run Frontend (React/Vite)
Open a new terminal, navigate to the frontend folder, and start the development server:
```bash
cd frontend/sistema-biblioteca
npm install
npm run dev
```
### API Endpoints (Examples)
|Method | Endpoint | Description |
|---:|:---:|---:|
| `POST` | `/api/token/` | Obtains the JWT access and refresh tokens for authentication. |
| `GET` | `/api/books/` | Retrieves a list of all available books in the catalog. |
| `POST` | `/api/loans/create/` | Registers a new book loan for an authenticated user. |

### Project Structure
```bash
/sistema-biblioteca
|
|-- /backend             --> Django Backend Core
|   |-- /api             --> REST Framework apps, views, and serializers
|   |-- /core            --> Django project settings & configuration
|   |-- manage.py        --> Django entry point
|   |-- requirements.txt --> Python dependencies
|   |-- .env             --> Database secrets (Hidden)
|
|-- /frontend            --> React + Vite Client
|   |-- /sistema-biblioteca
|       |-- /src         --> UI components, styles, and React logic
|       |-- package.json --> Node.js dependencies & scripts
|
|-- .gitignore           --> Git Ignore Rules (node_modules, .env, .venv)
|-- README.md            --> Project documentation
```
## About the Project
This is an academic project developed collaboratively in a team. My specific contributions focus on the Backend and API Architecture.

## Credits & Team
- Francisco Padilla: Backend Development & API Architecture - https://github.com/fcabrerapd

- Marlon Agustín Elías Nilo: Frontend Development & UI Integration - https://github.com/Sharpor1

- Lucian Muñizaga: Data Modeling & Database - https://github.com/LucianLH

## Screenshots
<img width="1877" height="931" alt="586633192-0b31b8dc-cc98-456e-83ed-74822c096e27" src="https://github.com/user-attachments/assets/84225f90-0b26-4cd1-8e24-c25826bb7845" />
<img width="1876" height="941" alt="586633409-da28de8a-2d9b-4e76-b8c1-f7211a79b599" src="https://github.com/user-attachments/assets/31128394-1ed5-4ab1-8978-da7d8f0883af" />

### License
This project is under the MIT License.
