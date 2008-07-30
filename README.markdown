# SASS Generator

This TextMate bundle allows you to easily generate CSS files from a folder of SASS files.

There are two self-explanatory commands included:

* Generate CSS (cmd-r)
* Generate CSS and refresh Firefox (cmd-shift-r)

## Installation

`cd ~/Library/Application Support/TextMate/Bundles/`  
`git clone git://github.com/postpostmodern/sass-generator-tmbundle.git "SASS Generator.tmbundle"`

## Example File Structure

* TM\_PROJECT\_DIRECTORY
  * public (optional)
    * index.html
    * css
      * all.css
      * print.css
      * screen.css
      * ie.css
      * sass
        * all.sass
        * print.sass
        * screen.sass
        * ie.sass
        * standard
          * default.sass
          * reset.sass
        * site
          * colors.sass
          * content.sass
          * footer.sass
          * forms.sass
          * global.sass
          * header.sass
          * nav.sass
          * sidebar.sass
          * ...
    * ...

## How It Works

When editing a SASS file, hitting cmd-r will walk up the directory tree until it finds the **sass** directory. 
It will convert each file in the **sass** dir to CSS and place the resulting .css files in the parent directory 
of the **sass** dir. It will not drill down into the subdirs of **sass**. Those subdirs (e.g. **site** and **standard**
should contain files that are included in the main SASS files (all.sass, print.sass, etc.).

