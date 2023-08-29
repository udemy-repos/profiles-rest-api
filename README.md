# Profile REST API

Profile REST API course code.

vagrant@ubuntu-bionic:/vagrant$ python3 -m venv ~/env

vagrant@ubuntu-bionic:/vagrant$ source ~/env/bin/activate

(env) vagrant@ubuntu-bionic:/vagrant$ pip install -r requirements.txt 
Collecting django==2.2 (from -r requirements.txt (line 1))
  Downloading https://files.pythonhosted.org/packages/54/85/0bef63668fb170888c1a2970ec897d4528d6072f32dee27653381a332642/Django-2.2-py3-none-any.whl (7.4MB)
    100% |████████████████████████████████| 7.5MB 108kB/s
Collecting djangorestframework==3.9.2 (from -r requirements.txt (line 2))
  Downloading https://files.pythonhosted.org/packages/cc/6d/5f225f18d7978d8753c1861368efc62470947003c7f9f9a5cc425fc0689b/djangorestframework-3.9.2-py2.py3-none-any.whl (911kB)
    100% |████████████████████████████████| 921kB 972kB/s
Collecting sqlparse (from django==2.2->-r requirements.txt (line 1))
  Downloading https://files.pythonhosted.org/packages/98/5a/66d7c9305baa9f11857f247d4ba761402cea75db6058ff850ed7128957b7/sqlparse-0.4.4-py3-none-any.whl (41kB)
    100% |████████████████████████████████| 51kB 4.0MB/s
Collecting pytz (from django==2.2->-r requirements.txt (line 1))
  Downloading https://files.pythonhosted.org/packages/7f/99/ad6bd37e748257dd70d6f85d916cafe79c0b0f5e2e95b11f7fbc82bf3110/pytz-2023.3-py2.py3-none-any.whl (502kB)
    100% |████████████████████████████████| 512kB 1.6MB/s
Installing collected packages: sqlparse, pytz, django, djangorestframework
Successfully installed django-2.2 djangorestframework-3.9.2 pytz-2023.3 sqlparse-0.4.4

(env) vagrant@ubuntu-bionic:/vagrant$ django-admin.py startproject profiles_project .

(env) vagrant@ubuntu-bionic:/vagrant$ python manage.py startapp profiles_api

Open the file:

profiles_project\settings.py

Add those lines:

INSTALLED_APPS = [
    'rest_framework'
    'rest_framework_authtoken',
    'profile_api',
]

Teste project

(env) vagrant@ubuntu-bionic:/vagrant$ python manage.py runserver 0.0.0.0:8000
