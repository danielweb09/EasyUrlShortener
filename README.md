# EasyUrlShortener

# About

**Easy Url Shortener** is an application developed in PHP, which is responsible for generating a new compressed URL, as well as monitoring accesses through this new address.

This is a simple project to use, just download, tweak the configuration file and you're done.

# Usability

Easy URL Shortener is a simple and functional application that requires no connection to the database or server settings.
Just extract the files to a folder on your server, and that's it, it's working, but you need to change a few lines in the App / config.php file to customize your information.

All URLs are persisted in text files, for each URLs a new one is created. Don't worry, the application ensures that there are no files with duplicate names. File names have the extension **.db**.

# Pages
- **App/config**: Configuration file, requires editing only once.
- **index.php**: Main file, responsible for directing.
- **login.php**: Authentication page, enter the password set in the **config.php** file.
- **panel.php**: Panel to insert, query and delete your URLs.
- **lougout.php**: Logout page, is called when clicked on the panel close button.
- **remove.php**: Page that removes a URL, is called when confirming the deletion of a URL.

# App/config.php

```php
<?php
  define("USERKEY", "a12345z");
  define("URLLENGTH", 5);
  define("SITEURL", "http://localhost/url?u=");
  define("PATH", "data");
?>
```

- **USERKEY**: Access password
- **URLLENGTH**: Amount of characters to be generated
- **SITEURL**: URL to your site, ex https://site.com/url?u=. Do not remove Query String /url?=u
- **PATH**: Directory where files will be created

# Manipulating the information

## Inserting
Go to the admin panel, at the top you must enter in the text field the URL you want to shorten, then click the **Create** button.
## Removing
Click the **Remove** button corresponding to the URL you want to remove. A dialog box should open, confirming the deletion.
## Query
Each table row corresponds to a URL, each column contains information:

- **ID**: filename and URL identifier.
- **Original URL**: Registered original URL, which will be redirected when accessing the new URL.
- **New URL**: New URL generated. By clicking on the text field the content is copied to the clipboard.
- **Access**: Number of accesses through the new URL.
## Updating and leaving the page
- To exit the page, simply click the **X** button located at the top right of the screen.
- To refresh the page, simply click the **R** button located at the top right of the screen.

# Author
This system was created in a series of PHP video classes for satellasoft.com portal, all classes are in portuguese-br.
www.satellasoft.com
