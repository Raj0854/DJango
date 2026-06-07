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
   Now you can add your static files to the appropriate subdirectories. For example, you can add a CSS file named `styles.css` to the `static/css` directory, a JavaScript file named `scripts.js` to the `static/js` directory, and an image named `logo.png` to the `static/images` directory.
5. **Use Static Files in Templates:**
    To use static files in your Django templates, you need to load the static template tag and then reference your static files using the `static` template tag. For example, in your HTML template, you can include your CSS and JavaScript files like this:
    
    ```html
    {% load static %}
    
    <link rel="stylesheet" type="text/css" href="{% static 'css/styles.css' %}">
    <script src="{% static 'js/scripts.js' %}"></script>
    <img src="{% static 'images/logo.png' %}" alt="Logo">
    ```
    
    In this example, we are loading the `styles.css` file from the `css` directory, the `scripts.js` file from the `js` directory, and the `logo.png` image from the `images` directory.
    