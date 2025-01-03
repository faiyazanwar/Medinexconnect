# Medinexconnect

## Overview
Medinexconnect is a Django-based web application designed to provide a seamless and efficient platform for connecting healthcare professionals and patients. The application supports a variety of features aimed at improving healthcare accessibility and communication.

## Features
- **User Authentication:** Secure user registration and login system.
- **Dynamic Content Management:** Manage healthcare-related content with ease.
- **Appointment Scheduling:** Enable patients to book appointments with healthcare providers.
- **Interactive Dashboard:** Role-based dashboards for administrators, doctors, and patients.
- **Search Functionality:** Advanced search to find healthcare professionals based on location and specialization.

## Prerequisites
Before running this project, ensure you have the following installed:
- Python 3.9+
- Django 4.x
- PostgreSQL (optional, depending on your database configuration)
- Git
- Pipenv or Pip

## Setup Instructions

### 1. Clone the Repository
```bash
git clone https://github.com/<your-username>/Medinexconnect.git
cd Medinexconnect
```

### 2. Create a Virtual Environment
Using `Pipenv`:
```bash
pipenv install
pipenv shell
```
Or using `venv`:
```bash
python -m venv env
source env/bin/activate  # On Windows: env\Scripts\activate
pip install -r requirements.txt
```

### 3. Configure Environment Variables
Create a `.env` file in the project root and set the required environment variables:
```
SECRET_KEY=<your-django-secret-key>
DEBUG=True
ALLOWED_HOSTS=localhost,127.0.0.1
DATABASE_URL=<your-database-url>
```

### 4. Apply Migrations
```bash
python manage.py migrate
```

### 5. Collect Static Files
```bash
python manage.py collectstatic
```

### 6. Run the Development Server
```bash
python manage.py runserver
```
Access the application at `http://127.0.0.1:8000/`.

## Deployment

### Deploying on Netlify
1. Add `runtime.txt` to specify Python version.
   ```
   python-3.9
   ```
2. Use `requirements.txt` for dependencies:
   ```bash
   pip freeze > requirements.txt
   ```
3. Add a `netlify.toml` file for configuration:
   ```toml
   [build]
   command = "pip install -r requirements.txt && python manage.py collectstatic --no-input"
   publish = "staticfiles"
   ```
4. Push changes to GitHub and link your repository to Netlify.

### Alternative Platforms
- **PythonAnywhere**
- **Render**
- **Railway**

## Project Structure
```
Medinexconnect/
|
├── manage.py          # Django's CLI utility
├── app_name/          # Your Django apps
├── static/            # Static files
├── templates/         # HTML templates
├── requirements.txt   # Python dependencies
└── runtime.txt        # Python version for deployment
```

## Reflections
This project taught us how to:
- Design scalable web applications using Django.
- Implement role-based authentication and authorization.
- Deploy applications on cloud platforms like Netlify and PythonAnywhere.

## Contributions
Contributions are welcome! To contribute:
1. Fork the repository.
2. Create a new branch: `git checkout -b feature-name`.
3. Commit your changes: `git commit -m 'Add feature-name'`.
4. Push to the branch: `git push origin feature-name`.
5. Open a pull request.

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.

## Contact
For questions or support, please contact:
- **Email:** faiyazanwar10@gmail.com
- **GitHub:** [faiyazanwar](https://github.com/faiyazanwar)

