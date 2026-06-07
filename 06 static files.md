### Static Files in Django
Static files are essential for any web application as they include CSS, JavaScript, images, and other assets that enhance the user experience. In Django, you can manage static files efficiently using the built-in static files framework. Here's how to set up and use static files in your Django project:
1. **Configure Static Files in settings.py:**
   Open your project's `settings.py` file and add the following configurations for static files:

   ```python
   # settings.py

   # Static files (CSS, JavaScript, Images)
   STATIC_URL = '/static/'
   STATICFILES_DIRS = [BASE_DIR / 'static']
   ```

   - `STATIC_URL` is the URL prefix for static files. You can change it if you want to serve static files from a different URL.
   - `STATICFILES_DIRS` is a list of directories where Django will look for static files. In this example, we are telling Django to look for static files in a directory named `static` located at the base of your project.    
   