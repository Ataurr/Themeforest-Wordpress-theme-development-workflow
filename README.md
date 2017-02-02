#A GOOD WORKFLOW SAVES YOUR TIMES & MONEY.

##Development Process

Develop the entire website in localhost
Commit changes to git and push to Bitbucket or github.
###1. Starter theme

Make Your Own Starter theme based On Underscores or Twenty Seventeen (New version of Wordpress default theme)  and Underscores (made by Automattic)

After Complete your starter theme save this on GitHub or Bitbucket.

###2.  Start Work For New Project

Cloning your starter theme (or a fork of it) into /wp-content/themes/ folder

###3.  Use task runner Like Grunt or gulp
For What ?
* prefixes to use in CSS
* Compressing my images
* Linting and minifying JS files
* Creating sprites
* Constantly refreshing my browser
* GULP RESOURCES
* Getting started with gulp
* An Introduction to Gulp.js
* Using Gulp for WordPress Theme Development
* WordPress theme development with Gulp, Bower, and Sass
* Youtube: https://www.youtube.com/results?sea...
* Automated WordPress Deployment with Grunt

###4.  Use Preprocessor  Like Sass Or Less
https://www.youtube.com/results?sea...

###4. Use git
Why Use Git: 
* Never have to remember which files you changed
* Super easy to keep all copies in sync
* Git Resource: 
* Learn Version Control with Git
* git - the simple guide
* tryGit
* Youtube: https://www.youtube.com/results?sea...
* For Github : Github for desktop.  For bitbucket: Sourcetree for bitbucket

####WORDPRESS-SPECIFIC GIT RESOURCES
* Version Controlling WordPress
* A WordPress & Git Workflow
* WordPress Development and Deployment With MAMP, Git and Dropbox

###5. Use Trello
Theme development is managed with Trello

###6. Clean Up Your Source Code 
* Messy source code is a developer’s nightmare. It makes finding things difficult, and it makes it extremely difficult for anyone else to work with it.
* Indent nested lines.
* Indent tabs always.
* Be consistent with formatting.
* Include concise, descriptive comments.
* Mind your line breaks.
* Strive for clean markup.

###7. Keep In Mind While Developing a theme:

Add this to ```wp-config.php define( 'WP_DEBUG', true );```

Escape Everything
// Use anytime HTML element encloses a section of data:
```php 
echo esc_html( $no_html );
```
// Use on all URLs, including those in the 'sr####c' and 'href' attributes of an HTML element:
```php
<img src="<?php echo esc_url( $escaped_url ); ?>" />
```
// Use for inline Javascript:
```php
<a href="#" onclick="<?php echo esc_js( $escaped_js ); ?>"><?php esc_html__( 'Click Here', 'text-domain' ); ?></a> 
```
// Use for an HTML attribute:
```php
<div class="<?php echo esc_attr( $escaped_class ); ?>">
```

Prefix Everything
// Functions
```php
function prefix_setup()
```####
// Classesclass 
```php
Prefix_Class {}
```
// Global Variables
```php
global $prefix_passengers;
```
// Action Hooks
```php
do_action( ‘prefix_start_engine’ );
```
// Filter Hooks
```php
$register = apply_filters( prefix_register );
```
// Non Third-Pary Script Handles
```php
wp_enqueue_script( 'prefix-functions', get_theme_directory_uri() . 'js/custom/functions.js' );
```
// Non Third-Pary Style Handles
```php
wp_enqueue_style( 'prefix-minified-style', get_theme_directory_uri() . 'style.min.css' );
```
// Images
```php
add_image_size( 'prefix-large', 800, 600 );
```
Do Not Prefix Third Party Scripts
// Incorrect 
```php
wp_enqueue_style( 'prefix-font-awesome', get_template_directory_uri() . '/css/font-awesome.css', array(), '4.2.0', 'all' );
```
// Corrrect 
```php
wp_enqueue_style( 'font-awesome', get_template_directory_uri() . '/css/font-awesome.css', array(), '4.2.0', 'all' );
```
// Incorrect 
```php
wp_enqueue_script( 'prefix-fitvids', get_template_directory_uri() . '/js/jquery.fitvids.js', array( 'jquery' ), '1.1.1', true );
```
// Corrrect 
```php
wp_enqueue_script( 'jquery-fitvids', get_template_directory_uri() . '/js/jquery.fitvids.js', array( 'jquery' ), '1.1.1', true );
```
After Complete theme: 

###8. Run Tests
* Run Theme Check. Must meet all Theme Check requirements
* Run Theme Mentor for themeforest: https://github.com/Ataurr/Theme-Men...

#### Check Plugins
* Developer Plugin
* Monster Widget Plugin.

