---
title: PalettePal
organisation: Personal
date: December 2021
duration: Dec. 2021
description: Generates colours palettes based on a search term. The search result images are processed with the k-means algorithm to identify the colour clusters.
---

# Context

A friend was making wireframes and needed a themed colour palette She could not find what she wanted on [Coolors](https://coolors.co/), as the functionalities available either did not meet her needs (randomly generated, trending palettes) or were not generic enough (colour palette based on only one image). 

# Project Overview 

To encapsulate a theme, I decided to use multiple reference images, which were scraped according to a provided search term with Selenium.  

Converting the image data for processing involved combining and compressing the images to  a single image of 200x200 pixels, and each pixel's RGB values were stored in an dataframe with pandas. The data was then processed via k-means clustering with scikitlearn.

# K-Means

K-Means clustering categorises the all the data points into an arbitrary number of clusters (k). In this project, each data point is a pixel represented by its RGB values, and the number of clusters was fixed at 5, to match the number of colours in a palette. The 5 centroid values returned by are the RGB values of the mean colour of each cluster. 

# Demo

![PalettePal Search: Orchid, 25 images ](/assets/images/works/PalettePal/searchOrchid25.png)

The search fields consist of the search query that describes the theme of the colour palette, and the number of reference images used to generate the palette. 

The default number of reference images is 10. The number of images can be set to an integer between 1 and 100 (inclusive), ensuring that each image is represented by at least 4 (2x2) pixels. 

![PalettePal Palette Result: Orchid, 25 images](/assets/images/works/PalettePal/paletteOrchid25.png)

The resulting palette contains 5 colours, following Coolor's number of colours for each palette. 

![PalettePal Reference Images: Orchid, 25 images](/assets/images/works/PalettePal/imagesOrchid25.png)

The reference images are shown below, to help the user have a overview of the images and better understand the choice of colours in the palette. The user could also use images (with the right permissions) from the search as assets.

# References
- [Understanding K-Means Clustering in Machine Learning](https://towardsdatascience.com/understanding-k-means-clustering-in-machine-learning-6a6e67336aa1)