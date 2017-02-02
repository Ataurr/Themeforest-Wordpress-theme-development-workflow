#A GOOD WORKFLOW SAVES YOUR TIMES & MONEY.

##Development Process

Develop the entire website in localhost
Commit changes to git and push to Bitbucket or github.
###1. Starter theme

Make Your Own Starter theme based On [Underscores](http://underscores.me/) or Twenty Seventeen (New version of Wordpress default theme)  and Underscores (made by Automattic)

After Complete your starter theme save this on [GitHub](https://github.com/) or [Bitbucket](https://bitbucket.org/).

###2.  Start Work For New Project

Cloning your starter theme (or a fork of it) into ```/wp-content/themes/``` folder

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
* [Youtube](https://www.youtube.com/results?search_query=how+to+use+Gulp)
* [Automated WordPress Deployment with Grunt](Automated WordPress Deployment with Grunt)

###4.  Use Preprocessor  Like Sass Or Less
* [Sass](https://www.youtube.com/results?sea...)

###4. Use git
Why Use Git: 
* Never have to remember which files you changed
* Super easy to keep all copies in sync

Git Resource: 
* [Learn Version Control with Git](http://www.git-tower.com/learn/)
* [git - the simple guide](http://rogerdudler.github.io/git-guide/)
* [tryGit](https://try.github.io/levels/1/challenges/1)
* [Youtube](https://www.youtube.com/results?search_query=how+to+use+git)

Desktop Tools
* For Github : [Github for desktop](https://desktop.github.com/).  
* For bitbucket: [Sourcetree for bitbucket](https://www.sourcetreeapp.com/)

####WORDPRESS-SPECIFIC GIT RESOURCES
* [Version Controlling WordPress](http://roybarber.com/version-controlling-wordpress/)
* [A WordPress & Git Workflow](http://plausiblethought.net/wordpress-git-workflow/)
* [WordPress Development and Deployment With MAMP, Git and Dropbox](http://code.tutsplus.com/tutorials/wordpress-development-and-deployment-with-mamp-git-and-dropbox--wp-25718)

###5. Use Trello
Theme development is managed with [Trello](trello.com).
Trello is a task management app that gives you a visual overview of what is being worked on and who is working on it.
The team sets about beta testing the theme. A list of bugs, tweaks and solutions is compiled, a hackathon is scheduled, and everything is completed by the developer.

http://lifehacker.com/how-to-use-trello-to-organize-your-entire-life-1683821040

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

#####Escape Everything
```php 
// Use anytime HTML element encloses a section of data:

echo esc_html( $no_html );

// Use on all URLs, including those in the 'sr####c' and 'href' attributes of an HTML element:

<img src="<?php echo esc_url( $escaped_url ); ?>" />

// Use for inline Javascript:

<a href="#" onclick="<?php echo esc_js( $escaped_js ); ?>"><?php esc_html__( 'Click Here', 'text-domain' ); ?></a> 

// Use for an HTML attribute:

<div class="<?php echo esc_attr( $escaped_class ); ?>">
```

#####**Prefix Everything**
```php
// Functions

function prefix_setup()


Prefix_Class {}

// Global Variables

global $prefix_passengers;

// Action Hooks

do_action( ‘prefix_start_engine’ );

// Filter Hooks

$register = apply_filters( prefix_register );

// Non Third-Pary Script Handles

wp_enqueue_script( 'prefix-functions', get_theme_directory_uri() . 'js/custom/functions.js' );

// Non Third-Pary Style Handles

wp_enqueue_style( 'prefix-minified-style', get_theme_directory_uri() . 'style.min.css' );

// Images

add_image_size( 'prefix-large', 800, 600 );
```

#####**Do Not Prefix Third Party Scripts**

```php
// Incorrect 
wp_enqueue_style( 'prefix-font-awesome', get_template_directory_uri() . '/css/font-awesome.css', array(), '4.2.0', 'all' );

// Corrrect 

wp_enqueue_style( 'font-awesome', get_template_directory_uri() . '/css/font-awesome.css', array(), '4.2.0', 'all' );

// Incorrect 

wp_enqueue_script( 'prefix-fitvids', get_template_directory_uri() . '/js/jquery.fitvids.js', array( 'jquery' ), '1.1.1', true );

// Corrrect 

wp_enqueue_script( 'jquery-fitvids', get_template_directory_uri() . '/js/jquery.fitvids.js', array( 'jquery' ), '1.1.1', true );
```
##Test theme

###8. Run Tests
* Run Theme Check. Must meet all Theme Check requirements
* Run Theme Mentor for themeforest: https://github.com/Ataurr/Theme-Men...

#### Check Plugins
* Developer Plugin
* Monster Widget Plugin.

