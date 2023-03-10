# PHP For Wordpress

### `global` keyword in PHP

The `global` keyword in PHP is used to make a global variable available within a function. When a variable is declared as global, it can be used inside the function as if it were declared within the function, even if it was declared outside of the function.

By default, variables declared within a function are local to that function and cannot be accessed outside of it. To access a global variable within a function, the "global" keyword must be used, followed by the name of the variable.

```
$variable = "Global Variable";

function myFunction() {
    global $variable;
    echo $variable;
}

myFunction(); // Outputs: Global Variable

```

In this example, the variable `$variable` is declared outside of the function and is made available within the function by using the "global" keyword. When the function is executed, the value of the global variable is echoed.



### `global` keyword usage in WordPress

In WordPress, the `global` keyword is used to make global variables available within a function. These variables are usually defined in the `WordPress core and contain` information about the `current state of the site`, such as the current user, the current post, or the current query. By using the `global` keyword, developers can access these variables within their own functions and use the information they contain to modify or enhance the behavior of their plugins or themes.

For example, the following code makes the `$post` global variable available within a function:

```
function my_function() {
    global $post;
    echo $post->post_title;
}

```

In this example, the `$post` global variable is made available within the function `my_function()` and the title of the current post can be displayed by echoing the `post_title` property of the `$post` object.

It's important to use the global keyword **sparingly** and only when necessary, as it can lead to code that is harder to maintain and debug. Whenever possible, try to use WordPress `actions and filters` to modify the behavior of the site rather than accessing global variables directly.



# Wordpress Plugin Developement

## Steps for creating a new plugin

1. Navigate to the WordPress installation???s `wp-content` directory.

2. Open the plugins directory.

3. Create a new directory and name it after the plugin (e.g. `plugin-name`).

4. Open the new plugin???s directory.

5. Create a new PHP file (it???s also good to name this file after your plugin, e.g. `plugin-name.php`)

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


### The `readme.txt` file in a WordPress plugin

The `readme.txt` file in a WordPress plugin is typically located in the root directory of the plugin. It is part of the plugin's code and is included in the plugin folder along with other important files such as the plugin's `main` file, the `uninstall.php` file, and any other necessary files.

The `readme.txt` file in a WordPress plugin is a simple text file that provides important information about the plugin. The purpose of the file is to help users understand what the plugin does, how to install and use it, and what the requirements are for running it. The `readme.txt` file also contains other important information such as the plugin version, author information, and a change log.

Additionally, the `readme.txt` file is used by the WordPress plugin repository to display information about the plugin on the plugin page, making it an important resource for users searching for plugins in the repository. By including a `readme.txt` file, plugin developers can provide users with a clear and concise description of the plugin's functionality and how it can be used.


### The `uninstall.php` file in a WordPress plugin

The uninstall.php file in a WordPress plugin is typically located in the root directory of the plugin. It is part of the plugin's code and is included in the plugin folder along with other important files such as the plugin's main file, the readme.txt file, and any other necessary files. When the plugin is uninstalled from a WordPress site, the uninstall.php file is automatically executed to allow the plugin to clean up after itself and remove any data or settings it created.

It provides a way for the plugin to clean up after itself, removing any data or settings it created during its time on the site. The file can be used to delete custom database tables, options, or settings that the plugin created, and to ensure that the plugin does not leave any unwanted data behind after it is uninstalled.

Having an `uninstall.php` file is optional but is considered a best practice in WordPress plugin development as it ensures that the plugin does not leave any unwanted data or files on the site after it has been uninstalled. Without an `uninstall.php` file, data and settings created by the plugin may remain on the site even after the plugin has been deleted, causing issues with other plugins or future installations.

### Adding empty index.php file in plugin directories

An empty `index.php` file in WordPress serves as a protection mechanism for the contents of the folder in which it is located. When a user tries to access the folder directly through the web, the web server will look for an index file in that folder, and if one is found, it will display the contents of that file. By including an empty index.php file in the folder, the contents of the folder become inaccessible, and the web server will instead return a 404 error when attempting to access the directory directly.

This is often used to prevent unauthorized access to sensitive information or to protect the contents of the folder from being directly accessible from the web. For example, in WordPress, the wp-content and wp-includes folders often include an empty index.php file to prevent users from directly accessing their contents. This helps to improve the security of the WordPress site by preventing access to important files and data.

<img width="768" alt="Screenshot 2023-01-29 at 9 58 40 PM" src="https://user-images.githubusercontent.com/204423/215342964-0a5b8e86-fd40-447b-9541-88eb6369ff5f.png">



<img width="1052" alt="Screenshot 2023-01-29 at 9 58 59 PM" src="https://user-images.githubusercontent.com/204423/215342968-74fd3cd5-cb9b-41fa-931e-571f171fb8b7.png">



# Reference

- https://developer.wordpress.org/plugins/intro/
