# INTRODUCTION

[FlaskBB](http://flaskbb.org) is a forum software written in python
using the micro framework Flask.


## FEATURES

* A Bulletin Board like FluxBB, DjangoBB in Flask
    * with Subforums
* Private Messages
* Admin Interface
* Group based permissions
* BBCode support
* Topic Tracker
* Unread Topics/Forums


## TODO

* **High Priority**:
    * Searching for members, posts,...
    * Move the topic in another forum
    * Fixing all bugs I encounter during development
* **Medium Priority**:
    * Database migrations
    * A own theme and make FlaskBB themable with Flask-Themes2
    * Localization (Babel)
    * Polls - I definitely want this! :)
* **Low Priority**:
    * Learn how to create a Plugin API so other developers can create plugins for FlaskBB
    * Figure out how to integrate it in another app


## DEPENDENCIES

* [Flask](http://flask.pocoo.org)
    * [Werkzeug](http://werkzeug.pocoo.org)
    * [Jinja2](http://jinja.pocoo.org)
* [Flask-SQLAlchemy](http://pythonhosted.org/Flask-SQLAlchemy/)
    * [SQLAlchemy](http://www.sqlalchemy.org/)
* [Flask-WTF](http://pythonhosted.org/Flask-WTF/)
    * [WTForms](http://wtforms.simplecodes.com/docs/1.0.4/)
* [Flask-Login](http://flask-login.readthedocs.org/en/latest/)
* [Flask-Mail](http://pythonhosted.org/flask-mail/)
* [Flask-Script](http://flask-script.readthedocs.org/en/latest/)

### OPTIONAL DEPENDENCIES
* [Pygmens](http://pygments.org/) - For code highlighting
* [Redis](http://redis.io/) - For counting the online guests


## INSTALLATION

* Create a virtualenv
    * Install virtualenvwrapper with your package manager or via
        * `sudo pip install virtualenvwrapper`

    * Add these lines to your `.bashrc`

            export WORKON_HOME=$HOME/.virtualenvs  # Location for your virtualenvs
            source /usr/local/bin/virtualenvwrapper.sh

    * Create a new virtualenv
        * `mkvirtualenv -a /path/to/flaskbb -p $(which python2) flaskbb`

    * and finally activate it
        * `workon flaskbb`

    * For more options visit the documentation [here](http://virtualenvwrapper.readthedocs.org/en/latest/index.html).

* Install the dependencies
    * `pip install -r requirements.txt`
* Create the development config
    * `cp flaskbb/configs/development.py.example flaskbb/configs/development.py`
* Create the database with some example content
    * `python manage.py createall`
* Run the development server
    * `python manage.py runserver`
* Visit [localhost:8080](http://localhost:8080)

## LICENSE

[BSD LICENSE](http://flask.pocoo.org/docs/license/#flask-license)

## ACKNOWLEDGEMENTS

[/r/flask](http://reddit.com/r/flask), [Flask](http://flask.pocoo.org) and it's [extensions](http://flask.pocoo.org/extensions/).
