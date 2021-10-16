# r-website

## Purpose

Experimenting with using RStudio simple website builder to build a website.

For details, see 

## Key Components

1. **_site.yml**: provides overall yaml header, meta data, navigation.
2. **index.Rmd**: required home page, with minimal yaml header, since it will work with _site.yml.
3. **other Rmd**: any other pages you want to include.
4. **site_builder.R**: holds **rmarkdown::render()** which is command that will build website.
5. **_site folder**: location where HTML files will automatically be placed. This is the content of the website. It's what you would upload to your web server. May include automatically-generated folders that contain supporting docs. These will need to be uploaded to the web server as well for the site to work as designed.

## How it Works

* Create **site pages using R markdown**, as normal. Only required page is **index.Rmd**.
* Set up **_site.yml** file to give the site title, set navigation, optionally includes or other info.
* Use **Builder** > **Build website** (if available) OR run **rmarkdown::render()** to generate HTML files for each Rmd file and organize in **_site** folder.
* Upload contents of **_site** folder to web server.
