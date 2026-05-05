# Security Notes

The original project contained development credentials and API keys directly in `settings.py`. In this cleaned version, those values have been replaced with environment variables.

## Changed Items

- `SECRET_KEY` is now read from `DJANGO_SECRET_KEY`.
- Stripe keys are now read from `STRIPE_SECRET_KEY` and `STRIPE_PUBLISHABLE_KEY`.
- Google Maps key is now read from `GOOGLE_MAPS_API_KEY`.
- PostgreSQL password is now read from `DB_PASSWORD`.
- Local setup uses SQLite by default.
- Login views no longer print submitted passwords in the console.

## Important

If the original Stripe or Google Maps keys were real, rotate/revoke them before publishing the repository publicly.
