### Create Templates
Templates in Django are used to define the structure and layout of your web pages. They allow you to separate the presentation layer from the business logic, making it easier to manage and maintain your code. To create templates in Django, follow these steps:
1. **Create a Templates Directory:**
   Inside your app directory, create a new directory called `templates`. This is where you will store your template files.

   ```bash
   mkdir appname/templates
   ```
    Replace `appname` with the name of your app.
2. **Create Template Files:**
   Inside the `templates` directory, you can create your HTML template files. For example, you can create a file called `index.html`:

   ```bash
    touch appname/templates/index.html
    ```
     Replace `appname` with the name of your app. You can add your HTML code to this file to define the structure of your web page.
3. **Configure Template Settings:**
   Open the `settings.py` file in your project directory and find the `TEMPLATES` setting. Make sure it is configured to include the `DIRS` option, which specifies the directories where Django will look for templates. You can add your app's templates directory to this list:

   ```python    
    TEMPLATES = [
         {
              'BACKEND': 'django.template.backends.django.DjangoTemplates',
              'DIRS': [os.path.join(BASE_DIR, 'appname/templates')],
              'APP_DIRS': True,
              'OPTIONS': {
                'context_processors': [
                     # ... other context processors
                ],
              },
         },
    ]
    ```
     Replace `appname` with the name of your app. This configuration tells Django to look for templates in the specified directory.
4. **Use Templates in Views:**
   In your views, you can use the `render` function to render your templates. For example, in your `views.py` file, you can create a view that renders the `index.html` template:

   ```python
    from django.shortcuts import render

    def index(request):
        return render(request, 'index.html')
    ```
     This view will render the `index.html` template when accessed. Make sure to map this view to a URL in your `urls.py` file to access it through the browser.
By following these steps, you can create and use templates in your Django project to define the structure and layout of your web pages.
