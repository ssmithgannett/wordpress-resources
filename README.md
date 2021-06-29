# WordPress Resources


Theme template:
* [Underscores.me](https://underscores.me)

Gutenberg Block dev:
* [create-guten-block](https://github.com/ahmadawais/create-guten-block)
* [Tutorial](https://css-tricks.com/learning-gutenberg-3-primer-with-create-guten-block/)
    * This is a good step-by-step and is what I used to get started. The node.js stuff can get pretty complicated...I've had to reinstall it a few times and it's always a pain...

Plugins:
* These are a lot more simple than blocks. Generally, you'll only need three files in a plugin's folder: PHP, CSS and JS. I put the CSS and JS in their own folders, and then name all the files identical to the folder name 
```sh
    Ex: this folder structure for the GPS Carriers' Application
    ├── gps-app.php
    ├── css
    |   └── gps-app.css
    └── js
        └── gps-app.js
```
