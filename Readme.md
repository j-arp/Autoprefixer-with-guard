#Why?

Working out how to have real time processing of css files in our cms. Plan is to use Guard and auto-prefixer-rails gem to do it.

#File structure

There is a **webroot** folder and a **themes** folder
Inside **themes** here is a **sites** folder. 
In sites there are two different site folders (mysite, and yoursite)
Inside those folders there a src and css folder. 

#Test it
Make sure guard and autoprefixer-rails are installed then start guard
This needs to work with symlink folders so create a symlink inside webroot and point to the themes folder
  ln -s ../themes . #from inside the webroot folder
As you edit files in src, they get moved to css with prefixes
