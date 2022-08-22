#Readme for django-react integration

1. Create Django App
    - django-admin startproject django_project

2. Create React App
    - npx create-react-app react-app

3. Move React App to Django directory

4. Configure Templates Engine
    - cd to react-app directory and run
        - npm run build
    - In Templates of Django settings.py:
        - os.path.join(BASE_DIR, 'react-app/build')

5. Url path configuration
    - go to urls.py and import TemplateView add a path 
        - from django.views.generic import TemplateView
        - path(''. TemplateView.as_view(template_name='index.html'))

6. Configure static files
    - In Settings.py add
        - STATICFILES_DIRS = [
            os.path.join(BASE_DIR, 'react-app/build/static'),
        ]

7. npm run build