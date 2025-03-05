Make dev server accessible:
```
python manage.py runserver 0.0.0.0:8000
```
add the following to your `settings.py`:
```
ALLOWED_HOSTS = ['10.40.4.56', '0.0.0.0']
```
The first IP (dev server) is for others to access the server and the second
is for yourself to access.

Django sessions https://youtu.be/N-R5mT-nIDk?si=9s9-AiEEnhKDa6q_