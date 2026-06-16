A web application for creating and managing polls.  

---

## Features

- **Create polls** – users can create custom polls with multiple options  
- **Vote** – simple voting interface for participants  
- **Results** – real-time voting results display  
- **Admin panel** – Django admin interface for managing polls and users  
- **SQLite database** – lightweight database for development

---

## Tech Stack

- **Language:** Python 3.12+  
- **Framework:** Django 5.1+  
- **Database:** SQLite (development) / PostgreSQL (production-ready)  
- **Frontend:** HTML, CSS, Django Templates  
- **Tools:** Git, pip, virtualenv

---

## Build & Run

```bash
# Clone the repository
git clone https://github.com/rdmx51-glitch/votings-site.git
cd votings-site

# Create and activate virtual environment
python -m venv venv
venv\Scripts\activate

# Install dependencies
pip install --upgrade pip
pip install -r requirements.txt

# Generate a secret key
python manage.py shell -c "from django.core.management.utils import get_random_secret_key; print(get_random_secret_key())"

# Paste the key into settings.py as SECRET_KEY, then run migrations
python manage.py migrate

# Create a superuser (optional)
python manage.py createsuperuser

# Run the development server
python manage.py runserver
