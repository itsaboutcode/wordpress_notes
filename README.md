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


### Adding readme.txt file in the root folder of plugin

The `readme.txt` file in a WordPress plugin is a simple text file that provides important information about the plugin. The purpose of the file is to help users understand what the plugin does, how to install and use it, and what the requirements are for running it. The `readme.txt` file also contains other important information such as the plugin version, author information, and a change log.

Additionally, the `readme.txt` file is used by the WordPress plugin repository to display information about the plugin on the plugin page, making it an important resource for users searching for plugins in the repository. By including a `readme.txt` file, plugin developers can provide users with a clear and concise description of the plugin's functionality and how it can be used.


### The `uninstall.php` file in a WordPress plugin


The `uninstall.php` file in a WordPress plugin is a script that runs when the plugin is uninstalled from a WordPress site. It provides a way for the plugin to clean up after itself, removing any data or settings it created during its time on the site. The file can be used to delete custom database tables, options, or settings that the plugin created, and to ensure that the plugin does not leave any unwanted data behind after it is uninstalled.

Having an `uninstall.php` file is optional but is considered a best practice in WordPress plugin development as it ensures that the plugin does not leave any unwanted data or files on the site after it has been uninstalled. Without an `uninstall.php` file, data and settings created by the plugin may remain on the site even after the plugin has been deleted, causing issues with other plugins or future installations.




# Reference

- https://developer.wordpress.org/plugins/intro/
