## Introduce
This project is on progress depending on Django Ledger project
## Quick Start

Django Ledger comes with a default CoA ready to use, or you could use your own. Make sure to select the appropriate
option when creating new entities.

* Install Django Ledger

```shell script
pip install django-ledger
```

To install Django Virtual Environment
```pip install pipenv```

* Or with pipenv:

```shell script
pipenv install django-ledger
```

* Add django_ledger to INSTALLED_APPS

```python
INSTALLED_APPS = [
    ...,
    'django_ledger',
    ...,
]
```

* Add URLs to your project:

```python
from django.urls import include, path

urlpatterns = [
    ...,
    path('ledger/', include('django_ledger.urls', namespace='django_ledger')),
    ...,
]
```

* Add Django SuperUser if necessary.

```shell
python manage.py createsuperuser
```

* Navigate to Django Ledger root view assigned in your project urlpattern setting.
* Use your user credentials.

# How To Set Up Django Ledger for Development

Django Ledger comes with a basic development environment already configured under __dev_env/__ folder not to be used
for production environments. If you want to contribute to the project perform the following steps:

1. Navigate to your projects directory.
2. Clone the repo from github and CD into project.

```shell
git clone https://github.com/arrobalytics/django-ledger.git && cd django-ledger
```

3. Install PipEnv, if not already installed:

```shell
pip install -U pipenv
```

4. Create virtual environment.

```shell
pipenv install
```

If using a specific version of Python you may specify the path.

```shell
pipenv install --python PATH_TO_INTERPRETER
```

5. Activate environment.

```shell
pipenv shell
```

6. Apply migrations.

```shell
python manage.py migrate
```

7. Create a Development Django user.

```shell
python manage.py createsuperuser
```

8. Run development server.

```shell
python manage.py runserver
```

# Run Test Suite

After setting up your development environment you may run tests.

```shell
python manage.py test django_ledger
```

# Screenshots

![django ledger entity dashboard](https://us-east-1.linodeobjects.com/django-ledger/public/img/django_ledger_entity_dashboard.png)
![django ledger balance sheet](https://us-east-1.linodeobjects.com/django-ledger/public/img/django_ledger_income_statement.png)
![django ledger income statement](https://us-east-1.linodeobjects.com/django-ledger/public/img/django_ledger_balance_sheet.png)
![django ledger bill](https://us-east-1.linodeobjects.com/django-ledger/public/img/django_ledger_bill.png)
![django ledger invoice](https://us-east-1.linodeobjects.com/django-ledger/public/img/django_ledger_invoice.png)
