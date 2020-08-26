# Django E-commerce Project

## Initial Setup

Resources
* [Django Project Boilerplate by justdjango](https://github.com/justdjango/django_project_boilerplate)
* [How to Create a Boilerplate for Django Project](https://www.youtube.com/watch?v=GEogao-tUec)

Steps:

1. Clone/pull/download the boilerplate repository
2. Create and activate virtualenv, then install dependencies.
```bash
conda create --name env_pyshop python=3.7
conda activate env_pyshop
pip install -r requirements.txt
```
3. Configure the .env variables
4. Rename the project with `python manage.py rename <currentprojectname> <newprojectname>`

This boilerplate includes:

1. Settings modules for deploying with Azure
2. Django commands for renaming your project and creating a superuser
3. A cli tool for setting environment variables for deployment

## Commands
```bash
prompt $g
conda remove --name env_pyshop --all
conda create --name env_pyshop python=3.7
conda activate env_pyshop
pip install -r requirements.txt
pip install flake8
pip freeze > requirements.txt
python manage.py rename demo djecommerce

# Migration
python manage.py makemigrations
python manage.py migrate
```


