# Gulp, Jade, Sass, jQuery and Bootstrap template

This repository is a quick jumpstart template for any web developer who is tired of setting up the same project over and over again.

It uses gulp to compile sass and jade files into a bundled css file and separate html files, but it also minifies your javascript files (which ufurtunately could not be concatenated because of a problem with Bootstrap not recognizing jQuery)

To utilize this template you'll need Node.js and npm to be installed on your system, since they are necessaty for Gulp to run
## How to use this template
1. Clone this repository from the terminal with the command ```git clone https://github.com/CodingHobby/Jade-Sass-Gulp-Template``` 
2. Go into the repository you just cloned
3. Run the command ```npm install```
4. Run the command ```npm start``` to start gulp, my task runner of choice, which will compile all of your files and start a live reloading server with CSS injection using BrowserSync, which will even let you see the website you created from different devices (which is a big part of web desing)

## File structure:
<pre>
.
├── app
│   ├── css
│   │   ├── 0-plugins
│   │   │   ├── bootstrap.scss
│   │   │   └── plugins-dir.sass
│   │   ├── 1-base
│   │   │   └── base-dir.sass
│   │   ├── 2-modules
│   │   │   └── modules-dir.sass
│   │   └── style.sass
│   ├── index.jade
│   ├── layouts
│   │   ├── head.jade
│   │   └── lorem.jade
│   └── scripts
│       ├── plugins
│       │   ├── bootstrap.min.js
│       │   └── jquery-3.1.1.min.js
│       └── scripts.js
├── dist
│   ├── build
│   │   ├── plugins
│   │   │   ├── bootstrap.min.js
│   │   │   └── jquery-3.1.1.min.js
│   │   └── scripts.js
│   ├── css
│   │   └── style.css
│   └── index.html
├── gulpfile.js
├── LICENSE
├── package.json
└── README.md

</pre>

The main source files are in the app folder, where you should keep your main jade web pages. 
This folder also has different sub directories:

+ ## CSS:

  + ## 0-plugins
    This is where you should be keeping your plugins saved as SCSS files (this template already comes with Bootstrap)

  + ## 1-base
    This is where you should be keeping all of your base files, such as fonts and general rules that are valid throughout the whole website

  + ## 2-modules
    This is where you should be keeping the SASS modules, which just contain style rules for a few classes, making the whole styling modular

+ ## Layouts:
  This is where you should be keeping all the jade layouts, such as navs and different sections of your website, so that your pages are more composable

+ ## Scripts:
  This is here you should keep all of your JS files

  + Plugins:
    This is where you should be keeping all of your plugins (this template already comes with both Bootstrap.js and jQuery)

+ ## Dist:
  This is where the compiled Jade files are going to end up.

  It has two subdirectories:

  + ## Build:
      This is where the minified scripts are going to end up

    + Plugins:
      This is where the minified plugins are going to end up

  + ## Css:
    This is where your only minified css file is going to end up


In the root directory you can also find:
+ The ```gulpfile.js``` file 
  which contains all of the gulp tasks
+ The ```package.json``` file 
  where you can edit your node.js configuration and the npm dependencies to install