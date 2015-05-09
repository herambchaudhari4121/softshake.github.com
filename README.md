Softshake's Website


# URLs : NO CONTENT OUTSIDE A YEAR

All HTML content has to be in a </YEAR/LG> directory.

For exemple, the association page for the 2013 edition has to be in the file `/2013/fr/association/index.html`.

This is to prevent several yearly editions.


# Technologies

## Github Pages

Workflow:

 - Modify sources
 - `git commit -m "Explanation of the modification"` 
 - `git push" (to put modifications on the server)
 - See online the modification !

You can also use the Github app : http://mac.github.com/ (or http://windows.github.com/)


## Markdown (Text Templating)

Github Pages supporting Markdown as default text templating engine to facilitate development.

It is HTML compliant : 

 - Or you can write full HTML code
 - Or you can use Markdown synthax (http://daringfireball.net/projects/markdown/syntax)
 - Or both.


## How to run the site locally

As Github Pages uses Jekyll (a blog engine).

How run locally (to test for example) :

 - Install Ruby on rails
 - `gem install github-pages`
 - `jekyll serve` (from the softshake root source directory)
 - `localhost:4000` (from your favorite browser)

GitHub uses **version 2.2.0** of Jekyll (see [this page](https://pages.github.com/versions/) for the version that is currently running. To keep up to date run `gem update github-pages`.

Configuration file: `_config.yml`.

# Structure
The web site is based on the [themeforest-6269713-eventify-one-page-conference-html5-template](http://themeforest.net/item/eventify-one-page-conference-html5-template/full_screen_preview/6269713)
## Site generation
The site is generated using layout and is structured as following:  

* index.html
* * _layout/2015_layout.html `<head> and script/css import`
* * * _layout/2015_home_en.html `navigation bar, intro section, contact and footer `
* * * * 2015/en/index.html `venue, speakers, .....`

## Files
All the files related to the template for the 2015 site is now grouped under `/templates/tf/`      

## Set map location
The location is set in the file [custom.js](templates/tf/js/custom.js) and search for `// Change this to your desired latitude and longitude`  
The location is set in two spots, first right after the comment and then in the `$('#map_canvas').gmap().bind('init', function ()`  
The text is already set in this function.

## Mail encryption
The mail for orga has been encoreypted using [this website](http://www.the-art-of-web.com/javascript/mailto/#output)
