# Django, uWSGI and Nginx in a container, using Supervisord

## NOTE
Modified version of https://github.com/dockerfiles/django-uwsgi-nginx

This Dockerfile allows you to build a Docker container with a fairly standard
and speedy setup for Django with uWSGI and Nginx.

Most of this setup comes from the excellent tutorial on 
https://uwsgi.readthedocs.org/en/latest/tutorials/Django_and_nginx.html

### Build and run
* docker build -t webapp .
* docker run -p 8000:80 -d webapp

### How to insert your application
app/ - move the files in the root of your project to this folder

uwsgi.ini - make sure "module" is pointing to your wsgi.py file relative to root of the project (app/)
