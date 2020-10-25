# Movie Web Application

## Description

A Web application that demonstrates use of Python's Flask framework. The application makes use of libraries such as the Jinja templating library and WTForms. Architectural design patterns and principles including Repository, Dependency Inversion and Single Responsibility have been used to design the application. The application uses Flask Blueprints to maintain a separation of concerns between application functions. Testing includes unit and end-to-end testing using the pytest tool.

## Installation

##### Installation via requirements.txt in Mac

```
% cd CS235-Assignment-2
% python3 -m venv venv
% source venv\bin\activate
% pip install -r requirements.txt
```

When using PyCharm, set the virtual environment using 'PyCharm'->'Preferences' and select 'Project:CS235-Assignment-2' from the left menu. Select 'Project Interpreter', click on the gearwheel button and select 'Add'. Click the 'Existing environment' radio button to select the virtual environment.

## Execution

##### Running the application

From the CS235-Assignment-2 directory, and within the activated virtual environment (see venv\bin\activate above):

`% flask run`

## Configuration

The ***CS235-Assignment-2/.env*** file contains variable settings. They are set with appropriate values.

- `FLASK_APP`: Entry point of the application (should always be wsgi.py).
- `FLASK_ENV`: The environment in which to run the application (either development or production).
- `SECRET_KEY`: Secret key used to encrypt session data.
- `TESTING`: Set to False for running the application. Overridden and set to True automatically when testing the application.
- `WTF_CSRF_SECRET_KEY`: Secret key used by the WTForm library.

## Testing

Testing requires that file ***CS235-Assignment-2/tests/conftest.py*** be edited to set the value of `TEST_DATA_PATH`. You should set this to the absolute path of the ***CS235-Assignment-2/movie_web_app/adapters*** directory.

E.g.

`TEST_DATA_PATH = os.path.join(os.sep, 'Users', 'yezi', 'CS235-Assignment-2', 'movie_web_app', 'adapters')`

assigns TEST_DATA_PATH with the following value (the use of os.path.join and os.sep ensures use of the correct platform path separator):

`Users\yezi\CS235-Assignment-2\movie_web_app\adapters`

You can then run tests from within PyCharm.

`% python -m pytest`

## Design Report

A design report is included in the master file.

`CS235Assignment2Journal.pdf`
