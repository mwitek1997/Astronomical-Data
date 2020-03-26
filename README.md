My team and I were tasked with collecting significant objects and sources in both R-Band & K-Band images taken from the National 
Optical Astronomy Observatory Deep Wide-Field Survey, in order to analyze each sources R-K color value, determine its stellarity
index through the use of a default neural network which we were provided with, to ultimately conclude which objects and sources
were stars or galaxies.

Through the creation of 4 useful catalogs in [SExtractor](https://www.astromatic.net/software/sextractor)...

  1. Catalog of objects/sources in the R-Band Image.
  2. Catalog of objects/sources in the K-Band Image.
  3. Catalog of object/source magnitude's in the R-Band.
  4. Catalog of object/source magnitude's in the K-Band.

We were able to sift through and find the brightest 15-20 objects/sources within each images catalog by...

  1. Locating the largest magnitude in the R-band magnitude catalog.
  2. Taking that magnitude's line number in the R-band magnitude catalog, and locating its respective x and y coordinates in the R-Band image catalog.
  3. With the use of [DS9](http://ds9.si.edu/site/Home.html), locate that specific object within the R-Band image using the found x and y coordinates.
  4. Using Frame>Match>Frame>WCS within [DS9](http://ds9.si.edu/site/Home.html), would locate that exact object/source within the K-Band image.
  5. Take down the K-Band x and y coordinates of the located source/image.
  6. Using the K-Band image catalog, we would locate those specific coordinates and take down the sources/objects magnitude.

The same was done working from the K-Band image to find the sources in the R-Band image. Once we located the brightest 
objects/sources in both the R-Band and K-Band images (largest magnitudes), we found that out of the 20 found, 5 of them matched
perfectly in both images. This left us 15 bright unique objects/sources found in the NOAO Deep Wide-Field Survey images.

Given that we now had both R-Band magnitudes and K-Band magnitudes, we were able to calculate the R-K color value. This value 
is strictly used to show if the object is more red (redder), or more blue (bluer). The results are shown in the presentation included in this
repository. What we found was that only object/source was more blue (bluer), while the rest were more red (redder). All this means is that while an
objects/sources R-band magnitude is brighter than its K-band magnitude, it tends to be bluer. While an objects/sources K-band magnitude is brighter than
its R-band magnitude, it tends to be redder.

When it came to the calculation of the stellarity index, we were provided with a default neural network which [SExtractor](https://www.astromatic.net/software/sextractor)
uses to calculate the stellarity index. What we found was that any stellarity index ranges between 0.00-1.00, values less than 0.5 are less stellar and thus a galaxy, and values 
greater than 0.5 are more stellar and thus a star. Our calculated values are provided in both the presentation and final report which are both provided in this repository. Our data
came to conlcude that out of our 15 unique bright objects/sources, seven of them were found to be star-like objects/sources and eight were found to be galaxy-like objects/sources.

All final patterns, trends, and further detailed explanations are included in the provided presentation and final report found in this repository.
