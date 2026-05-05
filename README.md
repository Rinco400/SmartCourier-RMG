# SmartCourier RMG — A Django-Based Delivery Management System for the Garment Industry

A Django-based bachelor project for managing courier and delivery services in the Ready-Made Garments (RMG) industry. The system focuses on delivery traceability, role-based user access, driver management, delivery requests, payment handling, and client-driver communication.

## Project Summary

This project was developed as a web-based e-courier management system. It supports multiple user roles such as system admin, client, driver, factory head, and industry users. The main purpose is to make delivery requests, driver assignment, delivery tracking, payment calculation, and status updates more organized for RMG-related logistics.

## Main Features

- User registration and login for clients and drivers
- Role-based access for admin, client, driver, factory head, and industry users
- Factory, industry, client, and driver information management
- Delivery request creation and status tracking
- Driver profile and availability management
- Destination-wise price setup
- Product type and delivery product management
- Client billing and invoice-related pages
- Driver location sharing and delivery tracking
- Contact/help functionality between users and admin
- Stripe payment integration placeholder
- Google Maps API integration placeholder

## Technology Stack

- Python
- Django
- Django Templates
- HTML, CSS, JavaScript
- Bootstrap
- SQLite for local development
- PostgreSQL optional through environment variables
- Stripe API placeholder
- Google Maps API placeholder

## Clean Repository Structure

```text
E-Courier-RMG-Industry/
├── account/                 # Client account, profile, contact, rating, billing views
├── delivery_service/        # Delivery product, delivery request, tracking, order update logic
├── driver/                  # Driver registration, profile, tasks, location sharing
├── e_courier/               # Main Django project settings, URLs, WSGI
├── factoryHead/             # Factory-head related views and routing
├── industry/                # Industry, location, and price setup models
├── notification/            # Notification app placeholder
├── users/                   # User app placeholder
├── templates/               # Global templates
├── static/                  # CSS, JavaScript, images, vendor assets
├── media/                   # Default profile image only; runtime uploads are ignored
├── docs/                    # Extra notes, screenshots, and references
├── manage.py
├── requirements.txt
├── environment.yml
├── .env.example
├── .gitignore
└── README.md
```


## Recommended Runtime

This project was originally built with an older Django version. For the smoothest local run, use Python 3.8 or 3.9 with the pinned dependencies in `requirements.txt`. Newer Python versions such as 3.12/3.13 may not support some older Django packages used in this project.

## Local Installation

Clone the repository:

```bash
git clone https://github.com/YOUR-USERNAME/E-Courier-RMG-Industry.git
cd E-Courier-RMG-Industry
```

Create and activate a virtual environment:

```bash
python -m venv .venv
```

For Windows PowerShell:

```powershell
.venv\Scripts\activate
```

For macOS/Linux:

```bash
source .venv/bin/activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Run database migrations:

```bash
python manage.py migrate
```

Create an admin user:

```bash
python manage.py createsuperuser
```

Start the development server:

```bash
python manage.py runserver
```

Open the project in your browser:

```text
http://127.0.0.1:8000/
```

## Environment Variables

Sensitive values were removed from the source code. Use `.env.example` as a reference and set your own values through environment variables.

Important variables:

```text
DJANGO_SECRET_KEY
DJANGO_DEBUG
DJANGO_ALLOWED_HOSTS
STRIPE_SECRET_KEY
STRIPE_PUBLISHABLE_KEY
GOOGLE_MAPS_API_KEY
DB_ENGINE
DB_NAME
DB_USER
DB_PASSWORD
DB_HOST
DB_PORT
```

By default, the project uses SQLite for easier local setup. PostgreSQL can be enabled by setting `DB_ENGINE=postgresql` and the related database variables.

## Original Bachelor Project Requirements Covered

1. Super admin can add factory information.
2. Admin can update client and driver information.
3. Admin can delete individual client and driver information.
4. Admin can search client, driver, and factory information.
5. Admin can add delivery product types.
6. Admin can add destination-based price settings.
7. Admin can update delivery type and price settings.
8. Admin can delete delivery type and price settings.
9. Admin can view client, driver, delivery, and industry information.
10. Client can register and manage profile information.
11. Client can search destination price information.
12. Client and driver can change passwords.
13. Client can view outstanding bill information.
14. Client can track delivery location.
15. Client can reset forgotten password.
16. Client can send delivery requests.
17. Client can give driver rating.
18. Client can make card-based payment through Stripe integration placeholder.
19. Driver can register and manage profile information.
20. Driver can respond to delivery requests.
21. Driver can view pickup history.
22. System admin can view old and latest delivery information.
23. Client and driver can contact admin.
24. System admin can edit delivery information.
25. System admin can print client and factory payment invoices.
26. System admin can view delivery tracking data.
27. System admin can add tracking data.
28. System admin can view active and inactive drivers.
29. System admin can update driver status.
30. Driver can share location with clients.

## Notes for GitHub Upload

Before pushing to GitHub, do not include local database files, virtual environments, cache files, `.env`, or user-uploaded media files. These are already covered in `.gitignore`.

## Author

## Contributors

- As Am Mehedi Hasan — Backend development, Django project structure, delivery tracking, documentation
- Xinia Apchora — Project planning, UI design support, testing, documentation, and feature validation
