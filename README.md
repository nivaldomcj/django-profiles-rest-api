# Profiles Rest API

This is the source code of a _toy_ Django project made during the course [Build a Backend REST API with Python & Django - Beginner](https://www.udemy.com/course/django-python),
taught by [@londonappdev](https://github.com/LondonAppDev) on Udemy. All credits go to the instructor.

## About

This simple REST API have the following functionality:

* Creating new profiles (```@POST /profile```)
* Logging in with a profile (```@POST /login```)
* Adding profile status updates (```@PATCH /profile```)
* Viewing users profile fields (```@GET /feed```)
* Searching for users profiles (```@GET /profile```)

There are some configuration files to run this project locally using [Vagrant](https://www.vagrantup.com/) and also some scripts for deploying it to an AWS instance.

## Setting up locally

To set up this project locally, make sure you have Vagrant installed and clone this repository:

~~~
git clone https://github.com/nivaldomcj/django-profiles-rest-api/
~~~

Make sure you're in the root repository folder and run the following command to set up the Vagrant box:

~~~
vagrant up
~~~

Access the created vagrant box by executing:

~~~
vagrant ssh
~~~

Then run the following commands to go to the root project folder and set up a Python Virtualenv with all project dependencies:

~~~
cd /vagrant/
python -m venv ~/env
source ~/env/bin/activate
pip install -r requirements.txt
~~~

Finally, run the necessary migrations and start the project by running:

~~~
python manage.py migrate
python manage.py collectstatic
python manage.py runserver 0.0.0.0:8000
~~~

Now you can access the project by opening any web browser and accessing localhost on port 8000.
