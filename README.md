# r-website

## Purpose

Experimenting with using RStudio simple website builder to build a website.

More details:

* https://rmarkdown.rstudio.com/lesson-13.html 
* https://bookdown.org/yihui/rmarkdown/rmarkdown-site.html

## Key Components

1. **_site.yml**: provides overall yaml header, meta data, navigation.
    + example here includes optional 'output' section to demonstrate additional functionality that can be incorporated (lots of other options available as well) - not required
2. **index.Rmd**: required home page, with minimal yaml header, since it will work with _site.yml.
3. **other Rmd**: any other pages you want to include.
4. **site_builder.R**: optional file that holds **rmarkdown::render()** which is command that will build website.
    + once you set up the project, close it, re-open it, you should have a **'Build'** tab on the right, just before 'Git' tab. There is a **'Build Website'** button on the Build tab that you can use to build/re-build the site as needed. 
5. **_site folder**: location where HTML files will automatically be placed. This is the content of the website. It's what you would upload to your web server. May include automatically-generated folders that contain supporting docs. These will need to be uploaded to the web server as well for the site to work as designed.

## How it Works

* Create **site pages using R markdown**, as normal. Only required page is **index.Rmd**.
* Set up **_site.yml** file to give the site title, set navigation, optionally includes or other info.
* Use **Builder** > **Build website** (if available - close/open R project if nec.) OR run **rmarkdown::render()** to generate HTML files for each Rmd file and organize in **_site** folder.
* Upload contents of **_site** folder to web server.
