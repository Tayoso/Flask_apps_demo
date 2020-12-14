# Flask

[TOC]

### What is Flask ?

> Flask is a micro web framework written in Python. It is similar to Django, however, Django is a [full stack framework](https://www.educba.com/python-frameworks/).

In simple terms, flask is similar to shiny but written in Python. Shiny is by far the quicker tool to get the job done and requires less knowledge about web based technologies. However, flask gives us much greater flexibility than could easily be achieved in shiny. 

Pinterest, [LinkedIn](https://www.educba.com/linkedin-website/) are one sites using Flask Framework. 

Mozilla, Instagram, The Washington Times, BitBucket use Django.

### Pros and Pros

- Shiny is quick and easy to use with minimum knowledge of CSS, HTML is required
- Flask apps thrive on front end development when the project/app requires it.
- Easy to integrate with AWS, Azure, GCP.
- Encourage the use of flask in creating apps especially as we are gradually starting to use python got some projects ...
- A complex web application utilizing ingenious SQL queries. Flask framework will save the day. 

### Installing Flask

Assuming you have git bash / shell command line already installed. 

- Flask is a module with a number of functions such as flash, redirect,render_template etc. Best to use Install Flask in your environ using this [Link](https://www.Flask.com/products/Flask-desktop)

To fully utilise the power of flask, knowledge of the following are important.

- Python
- SQLite
- Front-end Development
  - HTML & CSS. Tutorial [here](https://www.udemy.com/course/python-and-flask-bootcamp-create-websites-using-flask/)
  - Bootstrap. Tutorial [here](https://getbootstrap.com/docs/5.0/getting-started/introduction/ )
  - JS. Tutorial [here](https://www.codecademy.com/learn/introduction-to-javascript )
- Jinja Template. Tutorial [here](https://www.udemy.com/course/python-and-flask-bootcamp-create-websites-using-flask/)
- Celery 
- etc.

### Walkthrough

Install the requirements to run flask app in your 'venv' or 'pipenv'. Its safer to use 'pipenv' to avoid dependency issues, however this app was built using 'conda env'. 

```python
from flask import render_template, abort, url_for, flash, redirect, request, Blueprint, Response, session, jsonify, make_response
```

To run your basic flask app, its as simple as:

```python
from flask import Flask

app = Flask(__name__)

@app.route('/')
def index():
    return "This is an example app"
```

Its fine to have no key structure in place for small apps. Flask uses Blueprint to improve the structure of larger apps.

```bash
└── beanft
    ├── app.py
    ├── beanftsite
    │   ├── __init__.py
    │   ├── core
    │   │   └── views.py
    │   ├── data.sqlite
    │   ├── error_pages
    │   │   └── handlers.py
    │   ├── models.py
    │   ├── static
    │   │   ├── Chart.min.css
    │   │   ├── Chart.min.js
    │   │   ├── data_uploads
    │   │   │   ├── crimes-2017-18_SAS.csv
    │   │   │   ├── example_workorders_Sep18.csv
    │   │   │   ├── example_workorders_Sep18_TEST.csv
    │   │   │   ├── final_model.sav
    │   │   │   ├── iris.csv
    │   │   │   ├── iris_TEST.csv
    │   │   │   ├── mtcars.csv
    │   │   │   ├── pima-indians-diabetes.csv
    │   │   │   └── pima-indians-diabetes_TEST.csv
    │   │   ├── main.css
    │   │   └── profile_pics
    │   │       ├── default_profile.png
    │   │       └── loadingimage.gif
    │   ├── templates
    │   │   ├── account.html
    │   │   ├── base.html
    │   │   ├── chart.html
    │   │   ├── error_pages
    │   │   │   ├── 403.html
    │   │   │   └── 404.html
    │   │   ├── fit.html
    │   │   ├── index.html
    │   │   ├── login.html
    │   │   ├── plot.html
    │   │   ├── plot_2.html
    │   │   ├── plot_3.html
    │   │   ├── predict_data.html
    │   │   ├── register.html
    │   │   ├── train.html
    │   │   └── uploads.html
    │   ├── uploader
    │   │   ├── __init__.py
    │   │   └── views.py
    │   └── users
    │       ├── forms.py
    │       ├── picture_handler.py
    │       └── views.py
    ├── migrations
    │   ├── README
    │   ├── alembic.ini
    │   ├── env.py
    │   ├── script.py.mako
    │   └── versions
    │       └── 8fdc8a2ab450_works_fine.py
    ├── prompt.txt
    └── requirements.txt

```



### Things to remember

- Containers are ephemeral , however they have volumes (directories) that can be mounted up to the host. 

- To kill all containers 

  ```bash
  Flask container kill $(Flask ps -q)
  ```

## Invoking an api using cloud

`Flask build -t name .`

`Flask run --rm -p 80:80 name`

### An API using Heroku

This is a bit of complicated process but once we deploy the first one. We ultimately only change a few things in our Flask file and upload the app in the app folder.  

```
Flask build -t shinyapp .
```

```
Flask run -p 80:80 shinyapp
```
