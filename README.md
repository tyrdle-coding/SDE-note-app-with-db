# Notely 📓

A simple note-taking web app built with Python/Flask.

## Run Locally

```bash
pip install -r requirements.txt
python app.py
```

Visit http://localhost:5000

## Deploy to Render

1. Push this repo to GitHub
2. Go to https://render.com → New → Web Service
3. Connect your GitHub repo
4. Set the following:
   - **Runtime:** Python
   - **Build Command:** `pip install -r requirements.txt`
   - **Start Command:** `gunicorn app:app`
5. Add Environment Variables:
   - `APP_TITLE` = `Notely`
   - `NOTES_FILE` = `notes.json`
6. Click **Create Web Service**

Auto-deploy is enabled by default — every `git push` triggers a new deployment.

## Environment Variables

| Variable    | Description              | Default      |
|-------------|--------------------------|--------------|
| APP_TITLE   | Title shown in the UI    | Notely       |
| NOTES_FILE  | Path to JSON storage     | notes.json   |
| PORT        | Port to run on           | 5000         |