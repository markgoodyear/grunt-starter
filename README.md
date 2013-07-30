# Grunt Project
> Basic project setup with Grunt to standardise and structure projects.

### What's included?
- JShint, concatenate and minify JavaScript
- Compiles Sass with development and production options
- Sass sourcemaps*
- Rasterize `.svg` files
- Compress `.jpg/.jpeg`, `.png` and `.svg` files
- Livereload the browser on file changes

*To use sourcemaps, Sass 3.3.0 alpha must be installed: `sudo gem install sass --pre`

## Getting Started
Make sure you have Node.js and Grunt installed:

- Install Node.js from [http://nodejs.org](http://nodejs.org), or if you use [Homebrew](http://brew.sh/): `brew install node`
- Install Grunt by running `npm install -g grunt-cli`
- Install project dependancies with `npm install`. Make sure you're in the project root.

You may need to run the install commands as admin, so for Mac, use `sudo npm install`.

For more information on Grunt, see the [Getting Started](http://gruntjs.com/getting-started) guide.


## Directory Overview
```
ProjectRoot/
│
├── css/
│   ├── sass/
│   │   └── global.scss
│   └── <package-name>.css
│
├── img/
│   └── src/
│
├── js/
│   ├── src/
│   ├── vendor/
│   ├── <package-name>.js
│   └── <package-name>.min.js
│
├── node_modules/
│
├── Gruntfile.js
├── package.json
├──.jshintrc
├──.gitignore
├── index.html
└── README.md
```

### File Structure

**`css/`** —

`sass/global.scss` will be compiled too `css/<package-name>.css`. Import all project Sass files in this file.

**`img/`** —

Any `.png`, `.jpg`, `.jpeg` images placed here will be compressed and SVG files will be rasterised as PNG files upon `production` or `images` task [see tasks below for more info].

**`js/`** —

JavaScript files placed in `src/` will be tested with JShint, concatenated and minified to the root `js/` dir. `vendor/` should be used for vendor scripts, such as jQuery. Vendor scripts will not be tested with JShinted, concatenated or minified by default.

**`node_modules/`** —

Required dependancies are installed here, do not add to version control.

**`Gruntfile.js`** —

This file contains all the tasks to be run. It's heavily commented so check it out.

**`package.json`** —

Define project settings in this file. All dependancies are listed here too.

**`.jshintrc`** —

This file contains options for JShint.

**`.gitignore`** —

A standard `.gitignore` file for ignoring files/folders from being added the repo.

**`index.html`** —

Just a basic HTML file, not required for the project.

**`README.md`** —

You are here!

## Included Grunt Tasks

`grunt` —

JShint, concatenate and minify JS. Compile Sass with development settings (CSS not minified).

`grunt production` —

JShint, concatenate and minify JS. Compile Sass with production settings (CSS is minified), convert SVG to PNG, compress images.

`grunt images` —

Convert any images in `img/` from SVG to PNG. Also compress `.jpg`, `.jpeg` and  `.png` files.

`grunt watch` —

Watches files for changes and JShint, concatenate and minifies JS. Compiles Sass with development settings and reloads the page (requires the livereload browser plugin). Use `ctrl + c` to stop watching.

## Useful Resources

- [iTerm2](http://www.iterm2.com/#/section/home) — A better Terminal
- [http://integralist.co.uk/Grunt-Boilerplate.html](http://integralist.co.uk/Grunt-Boilerplate.html)
- [http://frederic-hemberger.de/artikel/grunt-buildtool-for-frontend-projects/](http://frederic-hemberger.de/artikel/grunt-buildtool-for-frontend-projects/)
- [http://mattbanks.me/grunt-wordpress-development-deployments/](http://mattbanks.me/grunt-wordpress-development-deployments/)
- [http://mondaybynoon.com/grunt-wordpress-theme-development/](http://mondaybynoon.com/grunt-wordpress-theme-development/)
- [http://blog.raddevon.com/becoming-self-sufficient-with-grunt-js/](http://blog.raddevon.com/becoming-self-sufficient-with-grunt-js/)
- [http://chrisawren.com/posts/Advanced-Grunt-tooling](http://chrisawren.com/posts/Advanced-Grunt-tooling)