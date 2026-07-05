# Sistema de Gestión de Biblioteca

![Python](https://img.shields.io/badge/python-%233670A0.svg?style=for-the-badge&logo=python&logoColor=ffdd54)
![Django](https://img.shields.io/badge/django-%23092E20.svg?style=for-the-badge&logo=django&logoColor=white)
![React](https://img.shields.io/badge/react-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB)
![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)
![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/postgresql-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white)

Una aplicación web full-stack desarrollada para gestionar catálogos de bibliotecas, usuarios y el flujo completo de préstamos y devoluciones de libros. El proyecto cuenta con una robusta API RESTful en el backend y una interfaz dinámica en el frontend.

## Características Principales
* **Gestión de Catálogo**: Administración completa de libros y documentos bibliográficos.
* **Control de Préstamos**: Seguimiento preciso de salidas, fechas de vencimiento y devoluciones.
* **Administración de Usuarios**: Gestión de perfiles con acceso basado en roles y autenticación mediante tokens JWT.
* **API RESTful**: Endpoints estructurados y seguros para la comunicación cliente-servidor.

## Stack Tecnológico
* **Backend**: `Python (Django)`, `Django REST Framework`, `Simple JWT`
* **Frontend**: `React`, `Vite`, `HTML5/CSS3/JavaScript`
* **Base de Datos**: `PostgreSQL`
* **Despliegue del Servidor**: `Gunicorn` & `Whitenoise`

## Requisitos Previos
Asegúrate de tener instalado lo siguiente en tu entorno local:
* [Python 3.10+](https://www.python.org/downloads/)
* [Node.js](https://nodejs.org/)
* [PostgreSQL](https://www.postgresql.org/)

## Guía de Inicio

### Clonar el repositorio

```bash
git clone https://github.com/fcabrerapd/sistema-biblioteca
cd sistema-biblioteca
```
### Configurar Variables de Entorno
Crea un archivo .env en la raíz del directorio backend y añade la configuración de tu base de datos y Django:
```bash
SECRET_KEY=your_django_secret_key_here
DEBUG=True
DB_NAME=biblioteca_db
DB_USER=postgres
DB_PASSWORD=your_password
DB_HOST=localhost
DB_PORT=5432
```
### Ejecutar Backend (Django)
Abre una terminal, navega a la carpeta backend e inicia el servidor:
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
### Ejecutar Frontend (React/Vite)
Abre una nueva terminal, navega a la carpeta frontend e inicia el servidor de desarrollo:
```bash
cd frontend/sistema-biblioteca
npm install
npm run dev
```
### Endpoints de la API (Ejemplos)
|Method | Endpoint | Description |
|---:|:---:|---:|
| `POST` | `/api/token/` | Obtiene los tokens de acceso y actualización JWT para la autenticación. |
| `GET` | `/api/books/` | Obtiene una lista de todos los libros disponibles en el catálogo. |
| `POST` | `/api/loans/create/` | Registra un nuevo préstamo de libro para un usuario autenticado. |

### Estructura del Proyecto
```bash
/sistema-biblioteca
|-- /backend
|   |-- /biblioteca_ERM
|   |-- /endpoints-postman
|   |-- /inventario
|   |-- /ops
|   |-- /usuarios
|   |-- .env.example
|   |-- Procfile
|   |-- manage.py
|   |-- requirements.txt
|
|-- /frontend
|   |-- /sistema-biblioteca
|   |-- package-lock.json
|
|-- .gitignore
|-- Pipfile
|-- Pipfile.lock
|-- README.md
|-- requirements.txt
```
## Sobre el Proyecto
Este es un proyecto académico desarrollado de manera colaborativa en equipo. Mis contribuciones específicas se centran en el Backend y la Arquitectura de la API.

## Créditos y Equipo
- Francisco Padilla: Desarrollo Backend y Arquitectura API - https://github.com/fcabrerapd

- Marlon Agustín Elías Nilo: Desarrollo Frontend e Integración UI - https://github.com/Sharpor1

- Lucian Muñizaga: Modelado de Datos y Base de Datos - https://github.com/LucianLH

## Capturas de Pantalla
<img width="1877" height="931" alt="586633192-0b31b8dc-cc98-456e-83ed-74822c096e27" src="https://github.com/user-attachments/assets/84225f90-0b26-4cd1-8e24-c25826bb7845" />
<img width="1876" height="941" alt="586633409-da28de8a-2d9b-4e76-b8c1-f7211a79b599" src="https://github.com/user-attachments/assets/31128394-1ed5-4ab1-8978-da7d8f0883af" />

### Licencia
Este proyecto está bajo la Licencia MIT.
