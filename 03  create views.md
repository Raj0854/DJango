### Create Views
In Django, views are responsible for handling the logic of your application and returning responses to the client. They can be thought of as the "controller" in the Model-View-Controller (MVC) architecture. To create views in your app, follow these steps:
1. **Create a View:**
   Open the `views.py` file in your app directory and define a view function. A view function takes a web request and returns a web response. Here's an example of a simple view that returns a "Hello, World!" message:

   ```python
   from django.http import HttpResponse

   def hello_world(request):
       return HttpResponse("Hello, World!")
   ```
    In this example, we import the `HttpResponse` class from `django.http` and define a view function called `hello_world` that takes a `request` object as an argument and returns an HTTP response with the message "Hello, World!".
2. **Map the View to a URL:**
   To make your view accessible via a web browser, you need to map it to a URL. Open the `urls.py` file in your app directory (if it doesn't exist, create it) and add the following code to define a URL pattern for your view:

   ```python
    from django.urls import path
    from . import views
    urlpatterns = [
        path('hello/', views.hello_world, name='hello_world'),
    ]
    ```
    In this code, we import the `path` function from `django.urls` and the `views` module from the current directory. We then define a URL pattern that maps the URL path `hello/` to the `hello_world` view function. The `name` parameter is optional but can be used to refer to this URL pattern in other parts of your code.
