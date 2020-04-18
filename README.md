# Warbler

An application inspired by Twitter.

## Getting Started

Clone and follow installation setup below to run the application on your local machine.

### Requirements

- Python 3.6+
- PostgreSQL

### Installing

Setup

Create a Python virtual environment and install all requirements from requirements.txt:
```
$ python3 -m venv venv
$ source venv/bin/activate
(venv) $ pip install -r requirements.txt
```

Set up database and seed database:
```
(venv) $ createdb warbler
(venv) $ psql warbler < seed.py
```

Start the server:
```
(venv) $ flask run
```

## Running Tests

Create test database and seed:
```
$ createdb warbler-test
$ psql warbler-test < seed.py
```

To run a file containing unittests, run command in terminal:
(FLASK_ENV set to production to not use debug mode during tests)
```
FLASK_ENV=production
python -m unittest 
```

To run a specific file:
```
python -m unittest [name-of-file.py]
```
