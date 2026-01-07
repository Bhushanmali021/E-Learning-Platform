# E-Learning Platform

E-Learning Platform 🚀
Full-stack Django-powered e-learning platform with user authentication, course management, payment integration, and admin dashboard. Perfect for Python developers and data professionals showcasing full-stack + BI skills.

## 🖥️ Frontend Preview

![E-Learning Platform Dashboard](https://private-user-images.githubusercontent.com/180542716/466581438-924f4f17-d153-475b-9c9f-00a72a31986a.png?jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3Njc3Nzg5NTEsIm5iZiI6MTc2Nzc3ODY1MSwicGF0aCI6Ii8xODA1NDI3MTYvNDY2NTgxNDM4LTkyNGY0ZjE3LWQxNTMtNDc1Yi05YzlmLTAwYTcyYTMxOTg2YS5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjYwMTA3JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI2MDEwN1QwOTM3MzFaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT03MWE1MzEzMDhkN2FiNzY3OGM2NjAxM2QwZDhkMzY3YmViOGIwZmRkOGQ2NmJhYzIyMjIxNzRjZjQzMzU5YzcxJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.zErongjL4yujt3VggAV10-1J9-O-tKjOojQRdNNRa9I)


---
| User Features                 | Admin Features            | Technical Features       |
| ----------------------------- | ------------------------- | ------------------------ |
| 🔐 Secure Signup/Login/Logout | 📚 Course CRUD Operations | ⚙️ Django ORM + SQLite   |
| 📖 Browse & Filter Courses    | 👥 User Management        | 💳 Payment Gateway Ready |
| 🛒 Course Enrollment          | 📊 Discount Management    | 📱 Responsive UI         |
| 💰 Payment with Discounts     | 🔧 Admin Dashboard        | 🔍 Search & Filtering    |

## Installation (Development)

## Clone repository
git clone https://github.com/Bhushanmali021/E-Learning-Platform.git
cd E-Learning-Platform

## Create virtual environment
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

## Install dependencies
pip install -r requirements.txt

## Database setup
python manage.py migrate
python manage.py createsuperuser

## Run development server
python manage.py runserver

##  Project Structure

E-Learning-Platform/
├── core/                 # Main Django app
│   ├── models.py        # User, Course, Enrollment models
│   ├── views.py         # Business logic
│   ├── forms.py         # Custom forms
│   ├── templates/       # HTML templates
│   └── admin.py         # Admin configuration
├── static/              # CSS, JS, Images
├── media/               # User uploads
├── requirements.txt     # Python dependencies
├── manage.py
└── README.md

## Key Django Features Implemented
## 1. Custom User Model

## models.py
class UserProfile(AbstractUser):
    is_instructor = models.BooleanField(default=False)
    date_joined = models.DateTimeField(auto_now_add=True)
    
## 2. Course Management
class Course(models.Model):
    title = models.CharField(max_length=200)
    price = models.DecimalField(max_digits=10, decimal_places=2)
    discount_price = models.DecimalField(null=True)
    is_published = models.BooleanField(default=True)
    
## 3. Enrollment System
class Enrollment(models.Model):
    user = models.ForeignKey(User, on_delete=CASCADE)
    course = models.ForeignKey(Course, on_delete=CASCADE)
    enrolled_at = models.DateTimeField(auto_now_add=True)
    is_completed = models.BooleanField(default=False)

## 💻 Developer Features
## Django Admin Customization
## admin.py
@admin.register(Course)
class CourseAdmin(admin.ModelAdmin):
    list_display = ['title', 'price', 'discount_price', 'is_published']
    list_filter = ['is_published', 'created_at']
    search_fields = ['title', 'description']

## Custom Template Tags
{% load custom_filters %}
{% discount_price course as final_price %}
Price: ${{ final_price }}

## 📊 Data Domain Integration Points
## Analytics Ready Models
📈 Enrollment Analytics: Completion rates, user progress
💰 Revenue Tracking: Course sales, discounts applied
👥 User Segmentation: Students vs Instructors
📚 Course Performance: Popularity, ratings

## Power BI Integration
1. Export enrollments to CSV
2. Connect via ODBC to SQLite
3. Build dashboards for:
   - Course completion rates
   - Revenue by category
   - User acquisition funnel

## 🔐 Security Features
✅ Password hashing (PBKDF2)
✅ CSRF Protection
✅ SQL Injection Prevention (ORM)
✅ XSS Protection (Django templates)
✅ Rate limiting ready
✅ HTTPS enforcement

##  🌐 API Endpoints (Future Expansion)
## DRF Ready Structure
GET    /api/courses/           # List courses
POST   /api/enrollments/       # Enroll user
GET    /api/user/courses/      # User enrolled courses
GET    /api/analytics/         # Dashboard stats

## 🧪 Testing Strategy
# Run tests
python manage.py test core.tests

** Coverage **
pip install coverage
coverage run manage.py test
coverage report

## 🔮 Future Enhancements
Phase 2: Video Streaming (HLS/DASH)
Phase 3: REST API (Django REST Framework)
Phase 4: Mobile App (React Native)
Phase 5: ML Recommendations
Phase 6: Gamification (Badges, Points)


