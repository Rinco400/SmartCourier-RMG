# Project Structure Notes

The original project was reorganized into a standard Django repository layout. The Django apps are now directly available at repository root beside `manage.py`.

## Main Apps

- `account`: user profile, registration, login-related custom views, billing, comments, ratings
- `delivery_service`: delivery request, product, order update, delivery tracking functionality
- `driver`: driver registration, profile, assigned delivery tasks, location sharing
- `industry`: industry, location, and price setup models
- `factoryHead`: factory-head dashboard and related views
- `notification`: notification app placeholder
- `users`: user app placeholder

## Removed from the final ZIP

- Python cache files: `__pycache__/`, `*.pyc`
- IDE files: `.idea/`
- Local database files: `db.sqlite3`
- Secret/local environment files: `.env`
- Runtime media uploads, except `media/default.jpg`
- Font/vendor font files and design-source files such as `.psd`
