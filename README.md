# Spatial Analytics Exam
Our repository for the code in our Spatial Analytics exam.

## Introduction
This README.md file supplies a brief overview of the contents of this repository that contains the code for our spatial analysis exam project. More information about the project can be found in our final paper.

## Prerequisites
If you want to test the code from scratch, you should download the full BBR dataset (here: https://ftp.sdfe.dk/main.html?download&weblink=2c950b3aadfeedc3b136df8525234819) and move it into the repository, where it should by default be named DK_INSPIRE_BBR.gpkg. We did not include it in our final repository because the file is massive (almost 5 GB). For more information about the dataset, see here: https://dataforsyningen.dk/data/3829. 
After having downloaded the file, you can run the creating_subsets.Rmd file and create the subsets (which are already included in our final submission). Afterwards you can run the main script, main.Rmd, and create visualizations identical to the ones in our paper. You can also just skip the first part, and only run the main script in order to create the visualizations, as it does not rely on the full dataset but the already existing subsets.

Most of the code runs fairly quick, it is only when looping through each region and getting the station/isochrone and building data that the code takes a long time to process (line 100).


## Structure
This section gives an overview of the different files in our repository.
* creating_subsets.Rmd: This file contains code that generates the two subsets from the full BBR dataset (requires that the full dataset is downloaded and in the main folder).
* exam_project.Rproj: This is the project file for this project.
* main.Rmd: This is the main script that processes the code and generates the visualisations. It is divided into several chunks, that each focus on a specific task. These are: preprocessing setup, data preparation, defining functions, data processing, combining geometry for mapping, creating an interactive leaflet map, creating a static ggplot2 map and lastly creating a bar chart.
* subset_nordjylland.gpkg: This is the Northern Jutland subset generated from the BBR dataset using bounding boxes from OSM in the creating_subsets.Rmd file.
* subset_nordsjaelland.gpkg: This is the Northern Zealand subset generated from the BBR dataset using bounding boxes from OSM in the creating_subsets.Rmd file.


## Authors
Alberte Lyngby Christensen & Peter Jørgensen
