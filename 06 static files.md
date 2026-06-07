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

2. **Create a Static Directory:**
   In your project directory, create a new directory called `static`. This is where you will store your static files such as CSS, JavaScript, and images.

   ```bash
   mkdir static
   ```
3. **Organize Static Files:**
   Inside the `static` directory, you can create subdirectories to organize your static files. For example, you can create `css`, `js`, and `images` directories:

   ```bash
   mkdir static/css static/js static/images
   ```
4. **Add Static Files:**
   Now you can add your static files to the appropriate subdirectories. For example, you can add a CSS file named `styles.css` to the `static/css` directory.
5. **Use Static Files in Templates:**
   To use static files in your Django templates, you need to load the static template tag and then reference the static files using the `static` template tag. Here's an example of how to include a CSS file in your template:

   ```html
   {% load static %}
    <link rel="stylesheet" type="text/css" href="{% static 'css/styles.css' %}">
    ```
    In this example, we are loading the `styles.css` file from the `static/css` directory. Make sure to adjust the path according to where your static files are located.