# E-Learning Platform

E-Learning Platform 🚀
Full-stack Django-powered e-learning platform with user authentication, course management, payment integration, and admin dashboard. Perfect for Python developers and data professionals showcasing full-stack + BI skills.

## 🖥️ Frontend Preview

![E-Learning Platform Dashboard](https://private-user-images.githubusercontent.com/180542716/466581438-924f4f17-d153-475b-9c9f-00a72a31986a.png?jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3Njc3Nzg5NTEsIm5iZiI6MTc2Nzc3ODY1MSwicGF0aCI6Ii8xODA1NDI3MTYvNDY2NTgxNDM4LTkyNGY0ZjE3LWQxNTMtNDc1Yi05YzlmLTAwYTcyYTMxOTg2YS5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjYwMTA3JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI2MDEwN1QwOTM3MzFaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT03MWE1MzEzMDhkN2FiNzY3OGM2NjAxM2QwZDhkMzY3YmViOGIwZmRkOGQ2NmJhYzIyMjIxNzRjZjQzMzU5YzcxJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.zErongjL4yujt3VggAV10-1J9-O-tKjOojQRdNNRa9I)


E-Learning-Platform/                 # Root Directory
│
├── core/                           # 🔥 Main Django Application
│   ├── migrations/                 # Database migrations
│   ├── __init__.py
│   ├── admin.py                    # Custom admin interface
│   ├── apps.py                     # App configuration
│   ├── models.py                   # User, Course, Enrollment models
│   ├── views.py                    # Class-Based + Function-Based Views
│   ├── forms.py                    # Custom forms & validation
│   ├── urls.py                     # App URL routing
│   └── templates/
│       ├── base.html               # Master layout (Bootstrap 5)
│       ├── courses/
│       │   ├── list.html           # Course catalog
│       │   └── detail.html         # Course details page
│       ├── accounts/
│       │   ├── login.html
│       │   ├── register.html
│       │   └── profile.html
│       └── dashboard.html          # User dashboard
│
├── static/                         # 🎨 Frontend Assets
│   ├── css/style.css               # Custom styles
│   ├── js/main.js                  # Interactive features
│   └── images/                     # Static images
│
├── media/                          # 📁 User Generated Content
│   ├── course_thumbnails/          # Course images
│   └── user_uploads/               # Profile pictures
│
├── elearning/                      # 🏗️ Main Django Project
│   ├── settings.py                 # Configuration
│   ├── urls.py                     # Main URL routing
│   └── wsgi.py                     # WSGI entry point
│
├── requirements.txt                # 📦 All Python dependencies
├── .env.example                    # 🔐 Environment variables
├── manage.py                       # ⚙️ Django management CLI
└── README.md                       # 📖 This documentation
