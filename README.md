# PHP For Wordpress

### Adding empty index.php file in plugin directories

An empty `index.php` file in a folder can serve as a protection mechanism for the files and directories within that folder. When a web server is configured to look for index files, if an index file is not found, the contents of the folder are displayed in a directory listing. By including an empty `index.php` file, the contents of the folder become inaccessible, and the web server will return a 404 error when attempting to access the directory directly. This can be used to prevent unauthorized access to sensitive information and to protect the contents of the folder from being directly accessible from the web.

<img width="768" alt="Screenshot 2023-01-29 at 9 58 40 PM" src="https://user-images.githubusercontent.com/204423/215342964-0a5b8e86-fd40-447b-9541-88eb6369ff5f.png">



<img width="1052" alt="Screenshot 2023-01-29 at 9 58 59 PM" src="https://user-images.githubusercontent.com/204423/215342968-74fd3cd5-cb9b-41fa-931e-571f171fb8b7.png">


# Wordpress Plugin Developement

## Steps for creating a new plugin

1. Navigate to the WordPress installation’s `wp-content` directory.

2. Open the plugins directory.

3. Create a new directory and name it after the plugin (e.g. `plugin-name`).

4. Open the new plugin’s directory.

5. Create a new PHP file (it’s also good to name this file after your plugin, e.g. `plugin-name.php`)

```
wordpress $ cd wp-content
wp-content $ cd plugins
plugins $ mkdir plugin-name
plugins $ cd plugin-name
plugin-name $ vi plugin-name.php
```

- `main` PHP file should include `header` comment what tells WordPress that a file is a plugin and provides information about the plugin.

- At a minimum, a header comment must contain the Plugin Name:

- https://developer.wordpress.org/plugins/plugin-basics/header-requirements/

```
/*
 * Plugin Name: YOUR PLUGIN NAME
 */
```

<img width="1154" alt="Screenshot 2023-01-29 at 9 48 38 PM" src="https://user-images.githubusercontent.com/204423/215341318-8058986c-0d55-4b37-a494-5a79ad0e905f.png">




# Reference

- https://developer.wordpress.org/plugins/intro/
