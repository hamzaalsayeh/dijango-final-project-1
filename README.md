# BookingApp — Django Appointment System

A clean appointment booking system built with Django. Clients browse providers, pick available time slots, and manage their bookings.

## Features

- Provider listing with available slot counts
- Time slot browsing grouped by date
- Booking with double-booking prevention
- Cancel appointments
- Email confirmation on booking (console in dev)
- Django Admin for managing providers, slots, and bookings
- User registration and login

## Project Structure

```
myproject/          Django project settings & URLs
myapp/              Main application
  models.py         Provider, TimeSlot, Booking
  views.py          All page logic
  urls.py           URL routing
  forms.py          RegisterForm, BookingForm
  admin.py          Admin configuration
  templates/myapp/  HTML templates
    base.html
    home.html
    provider_detail.html
    confirm_booking.html
    my_bookings.html
    cancel_confirm.html
    login.html
    register.html
```

## Quick Start

```bash
# 1. Install dependencies
pip install -r requirements.txt

# 2. Apply migrations
python manage.py migrate

# 3. Create a superuser (for admin panel)
python manage.py createsuperuser

# 4. Run the server
python manage.py runserver
```

## Adding Providers & Slots

1. Go to `http://127.0.0.1:8000/admin/`
2. Create a **User** for the provider
3. Create a **Provider** linked to that user
4. Create **TimeSlots** for that provider

## Tech Stack

- Python 3.11+
- Django 4.2
- SQLite (dev) / PostgreSQL (prod)
- Email via console backend (dev)
