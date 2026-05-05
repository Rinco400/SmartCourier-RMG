# GitHub Push Steps

Before pushing, test locally:

```powershell
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
python manage.py makemigrations --check
python manage.py migrate
python manage.py check
python manage.py runserver
```

If these commands run without errors, then push to GitHub.

Open PowerShell inside this cleaned project folder and run:

```powershell
git init
git add .
git commit -m "Initial clean upload of bachelor e-courier project"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/E-Courier-RMG-Industry.git
git push -u origin main
```

Replace `YOUR-USERNAME` with your GitHub username.

Before pushing, check the files that will be uploaded:

```powershell
git status
```

Important: do not upload `.env`, `db.sqlite3`, virtual environment folders, cache files, or runtime uploaded media files.
