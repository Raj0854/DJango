### Create an App
In Django, an app is a self-contained module that performs a specific function within your project. You can have multiple apps in a single project, and each app can be reused in different projects. To create an app, follow these steps:

1. **Create an App:**
   Use the following command to create a new app within your project:

   ```bash
   python manage.py startapp appname
   ```

   Replace `appname` with the desired name for your app. This command creates a new directory with the app name and the necessary files and directories inside.

2. **Register the App:**
   After creating the app, you need to register it in your project's settings. Open the `settings.py` file located in your project directory and find the `INSTALLED_APPS` list. Add your app to this list:

   ```python
   INSTALLED_APPS = [
       # ... other apps
       'appname',
   ]
   ```
    Replace `appname` with the name of your app.
    
