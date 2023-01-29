# PHP For Wordpress

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
