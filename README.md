# WordPress Resources


Theme template:
* [Underscores.me](https://underscores.me)
* Repos of the themes we've built:
    [Ask Mike](https://github.com/GannettDigital/ask-mike-theme)
    [Gannett.com](https://github.com/ssmithgannett/corp-site)
    [Architect](https://github.com/ssmithgannett/architect)
    [USAT Training](https://github.com/ssmithgannett/training)

Gutenberg Block dev:
* [create-guten-block](https://github.com/ahmadawais/create-guten-block)
* [Tutorial](https://css-tricks.com/learning-gutenberg-3-primer-with-create-guten-block/)
    * This is a good step-by-step and is what I used to get started. The node.js stuff can get pretty complicated...I've had to reinstall it a few times and it's always a pain...
* Blocks we've built:
    [Architect](https://github.com/ssmithgannett/architect-blocks)
    [Training Site Blocks](https://github.com/ssmithgannett/training-site-blocks)

Plugins:
* These are a lot more simple than blocks. Generally, you'll only need three files in a plugin's folder: PHP, CSS and JS. I put the CSS and JS in their own folders, and then name all the files identical to the folder name 
```sh
    'Ex: this folder structure for the GPS Carriers Application'
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
* I usually use plugins as extensions or one-off special cases, so the ones I build are typically pretty simple. If it you're trying to affect a large portion of a site, it might be better to revise part of the theme. 
    * In contrast, if you only need one small custom component on one page that will never be repeated, it's probably best to just write custom HTML into the WordPress page/post editor where it's needed.
* Repos of some plugins I've built:
    [Architect Photo Essay](https://github.com/ssmithgannett/architect-photo-essay) -- An extension for Architect Longform's theme to turn a page of photos into a gallery-style photo essay
    [GPS App](https://github.com/ssmithgannett/gps-app) -- Shortcode to place on corporate site for delivery drivers applications

