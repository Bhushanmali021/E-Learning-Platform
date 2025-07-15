# E-Learning Platform

A full-featured e-learning website built with Django, HTML/CSS, and Python. Supports signup/login, course browsing, payment gateway, discounts, and course enrollment.
<img width="1919" height="882" alt="project_image_1" src="https://github.com/user-attachments/assets/924f4f17-d153-475b-9c9f-00a72a31986a" />

---

## 🌟 Features

- **User**: Signup, login, logout
- **Courses**: Browse, filter, enroll, and resume learning
- **Payments**: Integrated payment gateway with discount support
- **Admin**: Add/edit courses via Django admin
- **Responsive UI**: HTML & CSS frontend

---

## Tech Stack

- **Backend**: Django (views, models, templates)
- **Database**: SQLite (default for Django)
- **Frontend**: HTML, CSS, (optionally JavaScript)
- **Dependencies**: Listed in `requirements.txt`

---

## Setup Instructions

### Prerequisites
- Python 3.8+
- pip
- (optional) Virtual environment: `python -m venv venv`

### Installation (Local)
```bash
git clone https://github.com/YourUser/E-Learning-Platform.git
cd E-Learning-Platform
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver

