# Warbler

An application inspired by Twitter.
Users can create an account, explore and follow/unfollow other users, edit their profile details, post "warbles", and like warbles.
This application began in complete collaboration/pair programmed with my peer, Richard Dowdy (we wrote and agreed on every step of the code in collaboration) and further additions were my own independently.

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

## Technologies 
- [Python3](https://docs.python.org/3/): backend server language
- [Flask](https://flask.palletsprojects.com/en/1.1.x/): Python framework
- [Flask SQLAlchemy](https://flask-sqlalchemy.palletsprojects.com/en/2.x/): Flask extension to support SQLAlchemy
- [Flask WTF](https://flask-wtf.readthedocs.io/en/stable/): Flask integration with WTForms
- [psycopg2](https://pypi.org/project/psycopg2/): PostgreSQL database adapter for Python
- [Jinja](https://palletsprojects.com/p/jinja/): Python template engine
- [bcrypt](https://pypi.org/project/bcrypt/): password hashing
