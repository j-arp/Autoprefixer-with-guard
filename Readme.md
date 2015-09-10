#Why?

Working out how to have real time processing of css files in our cms. Plan is to use Guard and auto-prefixer-rails gem to do it.

#File structure

There is a sites folder. 
In sites there are two different site folders (mysite, and yoursite)
Inside those folders there a src and css folder. 

Make sure guard and autoprefixer-rails are installed then start guard

As you edit files in src, they get moved to css with prefixes
