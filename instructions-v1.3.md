# How to Build a Simple WordPress Theme from Scratch

See: https://yoast.com/wordpress-theme-anatomy/



## Required Plugins

Please add these plugins to your Trade Fair site:

- [Query Monitor](https://wordpress.org/plugins/query-monitor/)
- [Show Current Template](https://downloads.wordpress.org/plugin/show-current-template.0.4.6.zip)
- [JACGWD CSS Reset Selector](https://github.com/JACGWD/CSS-Reset-Selector/archive/refs/heads/main.zip)




## Create a theme folder in wp-content
- Navigate to /htdocs/wp-content/themes/ and create a new folder called "your-name". 
- Ex: "billy-poppins". 
- Make sure to give it a name without spaces or capitalized letters.

## Create the theme preview artwork

- In Photoshop, create a blank document 1200px wide x 900px high
- Add any sort of background artwork you like for it
- Add the name of your theme as a layer on top
- Save the file as a PNG file inside your theme folder.
- The file must be called "screenshot.png".
- (Photo used in my demo is by [Noelle](https://unsplash.com/@noellejlee?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) on [Unsplash](https://unsplash.com/s/photos/scratching?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText))
  

## Create empty files in the theme folder

- Create a header.php file
- Create a footer.php file
- Create a functions.php file
- Create a index.php file
- Create an img folder for your style images (not content images - those are uploaded via the Wordpress interface and saved automatically into the wp-content/uploads folder)
- Create an fonts folder
- Create a style.css file

```
wp-content/themes/billypoppins
├── footer.php
├── functions.php
├── header.php
├── img
├── fonts
├── index.php
└── style.css

```


## CSS File
### Snippet 1: Add code to the CSS file
- Copy the code from Snippets/001.txt to your CSS stylesheet.
- Change the theme name and author to your own.
- Set the author URL to your GWD portfolio site
- Edit the Text Domain (the text domain is the key info that helps WP translate a site)

#### NOTE
- Your CSS as done in your previous GWD project would be considered incomplete for a "real" WordPress theme. 
- Consider using the [Natural Selection](https://github.com/frontaid/natural-selection) CSS starter file as a basis of a fully developed stylesheet.




## Breakdown of the HTML into component PHP pages

- Open the index.php, header.php and footer.php files

### Snippet 2:  Header
- In header.php, paste the code from snippets/002.txt


### Snippet 3: Footer
- In footer.php, paste the code from snippets/003.txt


### Snippet 4:  Index
- At the top of the index.php file, add the code from snippets/004.txt

### Snippet 5: Index
- At the very bottom of the index.php file, add the code from snippets/005.txt

### Snippet 6: Index
  
- In the middle in between the two tags you pasted, add the  code from snippets/006.txt

- Make sure to edit the text domain to match the one you wrote in the CSS file.


## Theme Functions File

The functions.php file is where most of the "magic" in Wordpress occurs. It contains the "functionality" of the theme. The other files in the theme define the appearance.


### Snippet 7: Function #1
#### Load the CSS stylesheet

- Add the code from snippets/007.txt to functions.php in order to "enqueue" the CSS file. This adds it automatically to the page as the theme loads. 


### Snippet 8: Function #2
#### Add the menu system

- Add the code from snippets/008.txt to the bottom of functions.php to enable the menu system. 
- You can add as many menus as you want, one per line, with unique names.



### Snippet 9: Add the menu to the page

- In header.php, add the code from snippets/009.txt inside the <nav> tag. This will load the menu in between teh nav tags.


## Test it

- Go to your Wordpress admin page
- Add and save (publish) a test page (you can add an image and some lorem ipsum)
- Add and save (publish) a test post (you can add an image and some lorem ipsum)
- Enable your theme in Appearance > Themes
- Go to Appearance > Menus and add (or select) a menu, check the box at the bottom to define it as the "header menu"
- Go visit your site home page

The web site should appear at the moment, with very basic HTML and no style whatsoever.



### Snippet 10:  Add the dynamic <head> tag content

- In header.php, paste the text from snippets/010.txt before the closing \</head> tag.
- In your stylesheet file, add a background color to the body (just to test to see if it works)



### Snippet 11:  Add the dynamic <body> tag content

- In footer.php, paste the text from snippets/011.txt before the closing \</body> tag.


### Snippet 12:  Add the search bar
- In header.php, add the code from snippets/012.txt right after the opening \<header> tag (before the nav).


## Add support for HTML 5 Semantic Tags, post thumbnails, custom title tags


### Snippet 13: Function #3
#### Add more custom features to the site. 

- Paste the snippets/013.txt code at the end of functions.php
- Remove  \<title>\</title> from header.php, as it will now be automatically generated

## Customize header.php

### Snippet 14: Add HTML language support
- Add the code from snippets/014.txt to the html tag (not !doctype html) in header.php
- Make sure to keep one space after the L of html before pasting

### Snippet 15: Replace UTF-8 tag with an automatically generated one

- In header.php, replace the entire \<meta charset="utf-8"> tag with the dynamic code from snippets/015.txt


### Snippet 16: Add automatic classes to the body tag
- In header.php, add the code from snippet/016.txt inside the body tag.
- Separate the new code from the Y of "body" with a space.


### Snippet 17: Add the H1 tag
- In index.php, just before the main tag, paste the code from snippets/017.txt



### Snippet 18: Add a clickable home link to the header
- In header.php, paste the code from snippets/018.txt immediately after the start of the header tag.
- In the header, the order of content will be:
- - branding div
- - nav tag with menu
- - search form
- All of these can be moved around according to your design choices

### Snippet 19: Add the tag line to the site

- In header.php, paste the code from snippets/019.txt immediately after the end of the branding div.
-  In the header, the order of content will be:
- - branding div
- - description div
- - nav tag with menu
- - search form
- All of these can be moved around according to your design choices


### Snippet 20: Add custom menus and copyright notice to the footer

- In footer.php, paste the code from snippets/020.txt immediately after the start of the footer tag.
- This will add two additional menus and the copyright notice of the blog into the footer.
- Remember to go to Appearance > Menus and define the menus, as well as click the box for their location.


###  Snippet 21: Add the sidebar

- In index.php, add the code from snippets/021.txt immediately after the closing main tag
- Create a new sidebar.php file inside your theme folder

###  Snippet 22:  Add the sidebar widget area
- Paste the code from snippets/022.txt into it.
- You can now go add widgets to your site in Appearance > Widgets


###  Snippet 23:  Add custom logo support

- In functions.php, add the code from snippets/023.txt inside the function billypoppins_theme_init() block
- Paste the new code in between "add_theme_support('title-tag');" and "add_theme_support('html5',"
- You will see new functionality within the customizer


###  Snippet 24:  Add custom logo functionality to the template

- In header.php, paste the code from snippets/024.txt at the top of the div class="branding" tag 


##  Snippet 25:  Build the color palette

- At the bottom of the styles.css stylesheet, paste the code from snippets/025.txt to have a color palette built with CSS variables.
- Customize the color palette as you wish.






# References: Additional Codes

See: https://codex.wordpress.org/Template_Tags#General_tags
     https://developer.wordpress.org/reference/functions/bloginfo/



### Code to Output the Path to Theme Folder
```
<?php echo get_stylesheet_directory_uri(); ?>
```
### Example to load decorative images from the theme's img folder:
```
<a href="#">
  <img src="<?php echo get_stylesheet_directory_uri(); ?>/img/twitter.svg" />
</a>
