### create Urls
In Django, URLs are used to map specific web addresses to views, which handle the logic for processing requests and returning responses. To create URLs in Django, follow these steps:
1. **Create a urls.py File:**
   Inside your app directory, create a new file called `urls.py`. This file will contain the URL patterns for your app.

   ```bash
   touch appname/urls.py
   ```
    Replace `appname` with the name of your app.
2. **Define URL Patterns:**
   Open the `urls.py` file you just created and define your URL patterns. You can use the `path` function to specify the URL pattern and the corresponding view. For example:

   ```python
    from django.urls import path
    from . import views

    urlpatterns = [
        path('', views.index, name='index'),
        # Add more URL patterns as needed
    ]
    ```
     In this example, the empty string `''` represents the root URL of your app, and it maps to the `index` view in your `views.py` file. You can add more URL patterns as needed to map different URLs to their respective views.
3. **Include App URLs in Project URLs:**
   After defining the URL patterns in your app's `urls.py` file, you need to
include these URLs in your project's main `urls.py` file. Open the `urls.py` file located in your project directory and add an `include` statement to include your app's URLs:

   ```python
    from django.contrib import admin
    from django.urls import path, include

    urlpatterns = [
        path('admin/', admin.site.urls),
        path('appname/', include('appname.urls')),
    ]
    ```
     Replace `appname` with the name of your app. This configuration tells Django to include the URL patterns defined in your app's `urls.py` file under the specified path (in this case, `appname/`).
4. **Access URLs in the Browser:**
   Once you have defined your URL patterns and included them in the project URLs, you can access them in the browser. For example, if you have defined a URL pattern for the `index` view as shown above, you can access it by navigating to `http://localhost:8000/appname/` in your web browser (assuming your development server is running on port 8000).
By following these steps, you can create and manage URLs in your Django project to map web addresses to their corresponding views.