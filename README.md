# wordpress_api_app
A simples wordpress api for block acess and protect your site

How does this code work? The code is written in PHP and works like an API key, which you can choose and change as you wish. Every time you log in to the WordPress dashboard, the code saves your account information in a cookie, and it is valid for one hour. This way, you can protect your site from external remote access and it is an extra security measure. As I am a web developer, this is my way of also preventing anyone from modifying the site that I am producing or making, and ensuring its security.

This is the main and almost unique file, written in PHP, it contains all the code, and should be placed in the wp-content folder > "folder you choose the name for the plugin" in my case; wp_api_app > here

This WordPress plugin protects access to the admin panel by requiring a secret key. It prevents unauthorized users from accessing wp-admin and wp-login.php.

How It Works
Secret Key Authentication:

The admin panel (wp-admin) and login page (wp-login.php) require a secret key.
The key can be provided via a URL parameter (?key=your-secret-key) or an Authorization header (Bearer your-secret-key).
Session Persistence:

Once the correct key is entered, a cookie is set, allowing access for 1 hour without needing to re-enter the key.
After the cookie expires, the user must authenticate again using the secret key.
Security Measures:

Direct access to the script is blocked if WordPress is not loaded.
The authentication mechanism ensures only authorized users can access the admin area.
Usage
Install and activate the plugin.

To access the admin panel, use:
https://yourwebsite.com/wp-admin/?key=your-secret-key

After entering the key once, you can navigate normally for 1 hour before needing to re-authenticate.

the secret pre-load apikey are: 12345678 and you can charge it in the code 
remenber: in my use : wp-content folder > "folder you choose the name for the plugin" in my case; wp_api_app > here code
