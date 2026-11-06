# Setup

## Initialization

### Set python version to 3.10.11

```bash
pyenv local 3.10.11
```

### Delete .git to start fresh repo
```bash
rm -rf .git
```

### Initialize and connect to GitHub repository

```bash
git init
```

```bash
git remote add origin git@github.com:dbalicky/FAIS601_m9.git
```

### Create and activate venv

```bash
python3 -m venv venv
source venv/bin/activate
```

### Install dependencies from requirements.txt

```bash
pip install -r requirements.txt
```

## Docker Setup

### Build docker compose file

Open docker desktop app

```bash
docker compose up --build
```

### Accessing postgres admin

Go to localhost:5050

- Enter username: admin@example.com

- Enter password: admin

### Add new server

1. Enter any name, i.e.: db

2. Click 'Add New Server'

3. Go to Connection tab

4. Enter host name: db

5. Server: 5432

6. Enter Maintenance database: fastapi_db

7. Enter Username and Password: postgres

8. Enable Save Password

9. Save

### Add tables

1. Navigate to db -> Databases -> fastapi_db -> Schemas

2. Open Tools -> Query Editor

3. Enter SQL code and execute

## Delete everything in docker conatiner

```bash
docker compose down -v
```

## Commnit and Push to GitHub

### Add and Commit changes
```bash
git add <file>

git commit -m '<description>'
```

### Push commits to GitHub
```bash
git push -u origin main
```

# Issues

### E2E Pytest Errors with Playwright

**Fixed by installing chromium**
```bash
python -m playwright install chromium
```