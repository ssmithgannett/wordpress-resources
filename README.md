# WordPress Resources


## Themes:
* Template: [Underscores.me](https://underscores.me)
* The main files we edit:
    * front-page.php: specific markup for what's designated as the home page in a site's customizer
    * page.php: for pages
    * template-parts > ....php: specific components for pages and posts, including the search page.
    * header.php: html head and the beginning of the body (header, navs, anything before the content)
    * footer.php: footer, site-wide scripts, etc 
    * inc > customizer.php: theme customizer options
    * functions.php: runs the site, essentially. Enables blocks, enqueues styles and scripts
    * style.css: theme css and metadata
    * 404.php: error page when incorrect URL is entered, ideally should direct user back home or somewhere to get them on track quickly

* Repos of the themes we've built:
    * [Ask Mike](https://github.com/GannettDigital/ask-mike-theme)
    * [Gannett.com](https://github.com/ssmithgannett/corp-site)
    * [Architect](https://github.com/ssmithgannett/architect)
    * [USAT Training](https://github.com/ssmithgannett/training)
    * [Native Ads - unreleased](https://github.com/ssmithgannett/native)

## Gutenberg Block dev:
* [create-guten-block](https://github.com/ahmadawais/create-guten-block)
* [Tutorial](https://css-tricks.com/learning-gutenberg-3-primer-with-create-guten-block/)
    * This is a good step-by-step and is what I used to get started. The node.js stuff can get pretty complicated...I've had to reinstall it a few times and it's always a pain...
* Blocks we've built:
    * [Architect](https://github.com/ssmithgannett/architect-blocks)
    * [Training Site Blocks](https://github.com/ssmithgannett/training-site-blocks)

## Plugins:
* These are a lot more simple than blocks. Generally, you'll only need three files in a plugin's folder: PHP, CSS and JS. I put the CSS and JS in their own folders, and then name all the files identical to the folder name 
```sh
    'Ex: this folder structure for the GPS Carriers Application'
    gps-app
    ├── gps-app.php
    ├── css
    |   └── gps-app.css
    └── js
        └── gps-app.js
```
* The PHP file contains the plugin metadata (version, title, author, etc) and the functions to run the plugin.
    * Enqueue scripts and styles
    * Set up shortcodes
    * Inject HTML to parts of the site
* I usually use plugins as extensions or one-off special cases, so the ones I build are typically pretty simple. If you're trying to affect a large portion of a site, it might be better to revise part of the theme. 
    * In contrast, if you only need one small custom component on one page that will never be repeated, it's probably best to just write custom HTML into the WordPress page/post editor where it's needed.
* Repos of some plugins I've built:
    * [Architect Photo Essay](https://github.com/ssmithgannett/architect-photo-essay) -- An extension for Architect Longform's theme to turn a page of photos into a gallery-style photo essay
    * [GPS App](https://github.com/ssmithgannett/gps-app) -- Shortcode to place on corporate site for delivery drivers applications

## Data stuff:
* We mainly use [Data.World](https://data.world) to query and format excel/csv into JSONs, though on occasion we have raw JSONs available on the web to parse (Google Sheets has a great API for public data...some teams have access to this...we're probably fine with Excel)
* I typically use a jQuery ajax function to call an API query though a PHP function...sounds more complicated than it is. 
* Ajax template for queries with no variable'
```
    
    "jQuery.ajax({
		url : 'path/to/php/file (must be on a server that can run php)',
		type : 'GET',
		success : function(data) {
			function-name(data);
		},
		error : function(request,error)
		{
			console.log("Request: "+JSON.stringify(request));
		}
	});// end ajax"
```
* Ajax template for queries with a variable:
```
    
    jQuery.ajax({
		url : 'path/to/php/file (must be on a server that can run php)',
		data: {
			'varibale': variable
		},
		success : function(data) {
	    	function-name(data);
		},
		error : function(request,error)
		{
			console.log("Request: "+JSON.stringify(request));
		}
	});// end ajax
```
* PHP templates:
    * [Directly call a d.w SQL query](https://github.com/ssmithgannett/php-to-d.w-queries/blob/master/no-var.php)
    * [Pass variable to query a d.w dataset](https://github.com/ssmithgannett/php-to-d.w-queries/blob/master/variable.php)
* [Encoder/decoder I use](https://meyerweb.com/eric/tools/dencoder/)

