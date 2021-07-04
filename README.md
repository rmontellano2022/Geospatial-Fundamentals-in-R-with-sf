# Geospatial Fundamentals in R with `sf` 

This is the repository for D-Lab's __Geospatial Fundamentals in R with `sf`__ workshop.

<!--
CAN ADD SLIDES AGAIN LATER
__View the Slides__:
- [Part 1 slides](https://dlab-berkeley.github.io/Geospatial-Fundamentals-in-R-with-sf/01-core_concepts_and_plotting.html#1) 
- [Part 2 slides](https://dlab-berkeley.github.io/Geospatial-Fundamentals-in-R-with-sf/02-spatial_analysis.html#1)
- [Part 3 slides](https://dlab-berkeley.github.io/Geospatial-Fundamentals-in-R-with-sf/03-raster_data.html#1)
--->
<!---
__View the Slides or RStudio Binders__:
HERE IS CODE FOR IF/WHEN WE IMPLEMENT BINDER
- [Part 1 slides](https://dlab-berkeley.github.io/Geospatial-Fundamentals-in-R-with-sf/docs/01-core_concepts_and_plotting.html#1), [![Part I](http://mybinder.org/badge.svg)](http://beta.mybinder.org/v2/gh/dlab-berkeley/Geospatial-Fundamentals-in-R-with-sf/docs/01-core_concepts_and_plotting/master?urlpath=rstudio)
- [Part 2 slides](https://dlab-berkeley.github.io/Geospatial-Fundamentals-in-R-with-sf/docs/02-spatial_analysis.html#1), [![Part II](http://mybinder.org/badge.svg)](http://beta.mybinder.org/v2/gh/dlab-berkeley/Geospatial-Fundamentals-in-R-with-sf/docs/02-spatial_analysis/master?urlpath=rstudio)
- [Part 3 slides](https://dlab-berkeley.github.io/Geospatial-Fundamentals-in-R-with-sf/docs/03-raster_data.html#1), [![Part III](http://mybinder.org/badge.svg)](http://beta.mybinder.org/v2/gh/dlab-berkeley/Geospatial-Fundamentals-in-R-with-sf/docs/03-raster_data/master?urlpath=rstudio)
--->

(For the old workshop, using the `sp` package, go [here](https://github.com/dlab-berkeley/Geospatial-Fundamentals-in-R-with-sp).)

--

# Workshop Goals

- __Part I: Core concepts, vector data, and plotting__
      - Basic geospatial concepts
      - Basic vector data
      - Geospatial data structures (the `sf` package)
      - Basic plotting (`base::plot` and the `ggplot3` package)
      - Managing coordinate reference systems (CRS)
      - Advanced plotting (the `tmap` package)
      - Map overlays
  - __Part II: Spatial analysis__
      - Spatial measurement queries
      - Spatial relationship queries
      - Buffer analysis
      - Spatial and non-spatial joins
      - Aggregation
      - Continued mapping practice
  - __Part III: Raster data__
      - Raster concepts
      - Raster data structures (the `raster` package) 
      - Mapping with raster and vector data
      - Spatial analysis of raster and vector data
      - Raster reclassification
      - Raster stacks and raster algebra 


**We assume that participants have working familiarity with the R language, including the topics covered in our [R-Fundamentals workshop](https://github.com/dlab-berkeley/R-Fundamentals) materials (though participants without this have still reported useful learning about geospatial concepts).**

# Installation Instructions

In preparation for the upcoming workshop you will need to install R and RStudio and the workshop materials.

1. Install R

Download R by clicking the link here: https://cloud.r-project.org/

Select your operating system and then click "base" (Windows users) or "R-4.0.3.pkg". Double-click this file once it has finished downloading and follow the instructions to install it.

2. Install RStudio

Download RStudio by visiting this link: https://rstudio.com/products/rstudio/download/

Scroll down and click the Download button beneath "RStudio Desktop - Open Source License - Free". Double-click this file once it has finished downloading and follow the instructions to install it.

3. Install the necessary packages
Install the following packages by typing:
install.packages(c(‘sp’, ‘sf’, ‘rgdal’, ‘rgeos’, ‘raster’, ‘ggplot2’, ‘tmap’, ‘tigris’, ‘tidycensus’))
Then check to ensure that you’re able to load them by typing
library(sp)
library(sf)
etc.


sp, sf, rgdal, rgeos, raster, ggplot2, and tmap, tigris and tidycensus.

4. Download the workshop materials

Download the workshop materials by visiting the GitHub repository: https://github.com/dlab-berkeley/Geospatial-Fundamentals-in-R-with-sf

To download the repository, click the green button in the top right hand corner that says "Code" and then select "Download ZIP". You can then unzip the contents of the downloaded folder somewhere accessible on your local computer (we recommend your Desktop).

We will take a few minutes at the start of the workshop to make sure everyone has R and RStudio installed and the workshop materials downloaded. Please feel free to email dlab-frontdesk@berkeley.edu or visit our help desk at https://dlab.berkeley.edu/frontdesk if you have any questions.

If you are a Git user, simply clone this repository by opening a terminal and typing: “git clone https://github.com/dlab-berkeley/Geospatial-Fundamentals-in-R-with-sf.git”


# Is R or RStudio not working on your laptop?

Attend the workshop anyway, we can provide you with a cloud-based solution (DataHub or Binder) until you figure out the problems with your local installation. 

If you have a Berkeley CalNet ID, you can run these lessons on UC Berkeley's DataHub by clicking this [link](https://datahub.berkeley.edu/hub/user-redirect/git-pull?repo=https%3A%2F%2Fgithub.com%2FAverysaurus%2FGeospatial-Fundamentals-in-R-with-sf&urlpath=rstudio%2F&branch=master). By using this link, you can save your work and come back to it at any time. When you want to return to your saved work, just go straight to DataHub (https://datahub.berkeley.edu), sign in, and you click on the Geospatial-Fundamentals-in-R-with-sf folder.
If you don't have a Berkeley CalNet ID, you can still run these lessons in the cloud, by clicking this [Binder button](https://mybinder.org/v2/gh/Averysaurus/Geospatial-Fundamentals-in-R-with-sf/HEAD?urlpath=rstudio). By using this button, you cannot save your work unfortunately. 

# Run the code! 

Make instructions

# How to get help?

* Within the language/tool itself
* Via Google searching
* On stackoverflow

# Resources

- The [Geocomputation with R](https://geocompr.robinlovelace.net/) textbook (Lovelace, Nowosad, and Muenchow, 2019) is an excellent resource for getting up and running.
- The [R sf package](https://r-spatial.github.io/sf/) webpage, especially the Articles tab of tutorials for getting started.
- The [`tmap` getting started](https://cran.r-project.org/web/packages/tmap/vignettes/tmap-getstarted.html) documentation is a great source of plotting support.
- The [`sf` vignettes](https://cran.r-project.org/web/packages/sf/vignettes/sf1.html) and [`sf` cheatsheet](https://github.com/rstudio/cheatsheets/blob/master/sf.pdf) are great resources for developing and debugging `sf` code.
- The [`raster` vignettes](https://cran.r-project.org/web/packages/raster/vignettes/Raster.pdf) should help you troubleshoot that package.


# About the UC Berkeley D-Lab

D-Lab works with Berkeley faculty, research staff, and students to advance data-intensive social science and humanities research. Our goal at D-Lab is to provide practical training, staff support, resources, and space to enable you to use R for your own research applications. Our services cater to all skill levels and no programming, statistical, or computer science backgrounds are necessary. We offer these services in the form of workshops such as R Fundamentals, one-to-one consulting, and working groups that cover a variety of research topics, digital tools, and programming languages.  

Visit the [D-Lab homepage](http://dlab.berkeley.edu/) to learn more about us. View our [calendar](http://dlab.berkeley.edu/calendar-node-field-date) for upcoming events, and also learn about how to utilize our [consulting](http://dlab.berkeley.edu/consulting) and [data](http://dlab.berkeley.edu/data-resources) services. 

(include definition of IOKN2K!)

# Other D-Lab R Workshops
* [R Advanced Data Wrangling: Parts 1-2](https://github.com/dlab-berkeley/advanced-data-wrangling-in-R)		
* [R Data Wrangling and Manipulation](https://github.com/dlab-berkeley/R-wrang)	
* [R Functional Programming](https://github.com/dlab-berkeley/R-functional-programming)		
* [R Fundamentals: Parts 1-4](https://github.com/dlab-berkeley/R-Fundamentals)	
* [R Introduction to Deep Learning: Parts 1-2](https://github.com/dlab-berkeley/Deep-Learning-in-R)		
* [R Introduction to Machine Learning with tidymodels: Parts 1-2](https://github.com/dlab-berkeley/Machine-Learning-with-tidymodels)		
* [R Visualization](https://github.com/dlab-berkeley/R-graphics)		
* [Python Geopandas: Parts 1-3](https://github.com/dlab-berkeley/Geospatial-Fundamentals-in-Python)		


# Contributors 


----
<div style="display:inline-block;vertical-align:middle;">
<a href="https://dlab.berkeley.edu/" target="_blank">
<img src ="https://dlab.berkeley.edu/sites/default/files/logo.png" width="60" align="left" border=0 style="border:0; text-decoration:none; outline:none">
</a>
</div>
<div style="display:inline-block;vertical-align:middle;align:left">
    <div style="font-size:larger">D-Lab @ University of California - Berkeley
    </br>
    <a href="https://dlab.berkeley.edu" target="_blank">https://dlab.berkeley.edu</a>
    </br>
    &nbsp;
    </div>
</div>

