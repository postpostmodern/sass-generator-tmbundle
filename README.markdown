# SASS Generator

This TextMate bundle allows you to easily generate CSS files from a folder of SASS files.

There are two self-explanatory commands included:

* Generate CSS (cmd-r)
* Generate CSS and refresh Firefox (cmd-shift-r)

## Installation

`cd "~/Library/Application Support/TextMate/Bundles/"`  
`git clone git://github.com/postpostmodern/sass-generator-tmbundle.git "SASS Generator.tmbundle"`

## Example File Structure
 
    TM_PROJECT_DIRECTORY
    `-- public
        |-- contact.cfm
        |-- contact_process.cfm
        |-- contact_thanks.cfm
        |-- copyright.cfm
        |-- css
        |   |-- all.css
        |   |-- ie.css
        |   |-- print.css
        |   |-- screen.css
        |   `-- sass
        |       |-- all.sass
        |       |-- ie.sass
        |       |-- print.sass
        |       |-- screen.sass
        |       |-- site
        |       |   |-- asides.sass
        |       |   |-- colors.sass
        |       |   |-- content.sass
        |       |   |-- global.sass
        |       |   |-- header.sass
        |       |   |-- ie.sass
        |       |   `-- nav.sass
        |       `-- standard
        |           |-- reset.sass
        |           `-- default.sass
        |-- img
        |-- index.html
        `-- js

## How It Works

When editing a SASS file, hitting cmd-r will cause TextMate to walk up the directory tree until it finds the **sass/** directory. 
It will convert each file in the **sass/** dir to CSS and place the resulting .css files in the parent directory 
of the **sass/** dir (usually **css/**). It will not drill down into the subdirs of **sass/**. Those subdirs (e.g. 
**site/** and **standard/**) should contain files that are included in the main SASS files (all.sass, print.sass, 
etc.).

