# Rumi Press Expense Tracker

A Django web application that helps the Rumi Press team track book distribution expenses while migrating away from spreadsheets.

## Why this project exists
- Centralize expense tracking for book categories (Business Analytics, Python, Data Science, Math, etc.).
- Increase data security with authenticated access.
- Provide CRUD workflows for categories, books, and their expenses.
- Generate visual and tabular reports that summarize costs by category.

## Tech stack
- Python 3.10+
- Django 4.2
- SQLite (development) with option to swap for PostgreSQL later
- HTML/CSS and Django templates (Bootstrap planned for styling)

## Repository layout
- `manage.py` — Django project entry point.
- `requirements.txt` — frozen dependencies for the virtual environment.
- `rumipress/` — project settings, URLs, ASGI/WSGI configuration.
- `expenses/` — main application package (models, views, templates to be added).
- `.venv/` — local virtual environment (ignored by Git).

## Getting started
1. Clone the repo and `cd money-tracking`.
2. Create the virtual environment: `python -m venv .venv`.
3. Activate it: `.venv\Scripts\Activate.ps1` (PowerShell).
4. Install dependencies: `python -m pip install -r requirements.txt`.
5. Apply database migrations: `python manage.py migrate`.
6. Create a superuser (admin login): `python manage.py createsuperuser`.
7. Run the development server: `python manage.py runserver`.

## Learning milestones
- [ ] Finalize the data model for categories, books, and expenses.
- [ ] Register models in Django admin with useful list displays and filters.
- [ ] Build public CRUD views/forms for categories and books.
- [ ] Add authentication (login/logout, access control for CRUD screens).
- [ ] Implement spreadsheet import (CSV/XLSX) into models with a management command.
- [ ] Produce an expense report view grouped by category (table first, charts later).
- [ ] Polish UI/UX and document deployment considerations.

## Feature roadmap
- Data modeling: design relationships, add default ordering, validations, and seed data.
- Admin scaffolding: customize list pages, add inlines to manage related records faster.
- CRUD interface: class-based views, URLs, templates, and form validation.
- Data import: script/management command to read spreadsheet rows and upsert records safely.
- Reporting: aggregate expenses per category using Django ORM annotations; consider a chart library once tables work.
- Authentication & authorization: protect views with `login_required`, explore staff-only permissions.

## Git workflow reminders
1. Keep `main` clean; create feature branches (e.g., `feature/data-models`).
2. Make small, focused commits with descriptive messages.
3. Run `python manage.py test` (or targeted checks) before each commit.
4. Push branches to GitHub and open pull requests if collaborating.

## Helpful commands
```
python manage.py makemigrations
python manage.py migrate
python manage.py shell
python manage.py runserver
python manage.py test
```

## Resources for learning
- Django documentation: https://docs.djangoproject.com/en/4.2/
- Django tutorial (official): https://docs.djangoproject.com/en/4.2/intro/
- ORM queries cheat sheet: https://docs.djangoproject.com/en/4.2/topics/db/queries/
- Django admin customization guide: https://docs.djangoproject.com/en/4.2/ref/contrib/admin/
- Corey Schafer Django playlist: https://www.youtube.com/playlist?list=PL-osiE80TeTvqhHnEgx3l4vX2AqABj9xN

Update this README as you complete milestones and learnings so future employers can follow your progress.
