# Flask ecommerce app

Here is an ecommerce app I built with Flask and SQLAlchemy. Fake data is supplied by Faker.
I followed this tutorial from ["Pretty Printed"](https://courses.prettyprinted.com/p/flask-sqlalchemy-basics)


# Setup

I assume Python 3.x or higher is installed.

# Tech used

```
click==7.1.2
Faker==4.1.1
Flask==1.1.2
Flask-SQLAlchemy==2.4.3
itsdangerous==1.1.0
Jinja2==2.11.2
MarkupSafe==1.1.1
python-dateutil==2.8.1
six==1.15.0
SQLAlchemy==1.3.17
text-unidecode==1.3
Werkzeug==1.0.1
```

# Getting it to run

For this project I am using pyenv (you can read about this here: https://github.com/pyenv/pyenv). For example (using linux terminal)

## Set up a new environment
`$ pyenv virtualenv 3.8.1 exampleenv `

## Activate environment
`$ pyenv activate exampleenv`

In order to install all nececsary libraries please:

`$ pip install -r requirements.txt`

## Export flask app

Export the app in your terminal with

`$ export FLASK_APP=flaskapp.py`

Run in debug mode with

`$ export FLASK_DEBUG=1`

## Create your database

To create your database using faker access the `flask shell` and run

```
>>> from flaskapp import create_random_data
>>> create_random_data
```
(You may have to exit and repeat this step if there are conflicts)


# Example query

If you would like to see the revenue you have earned in the past 30 days you can run these commands in the shell:

```
from flaskapp import revenue_in_last_x_days
revenue_in_last_x_days() # the default number of days is 30
```

# Limitations

- This app is not tested
- It could also be improved by diving the code into individual files for models etc