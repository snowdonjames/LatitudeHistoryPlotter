LatitudeHistoryPlotter
======================

> github.com/snowdonjames/LatitudeHistoryPlotter

This python script parses kml data file(s) ( see http://en.wikipedia.org/wiki/Keyhole_Markup_Language ) and renders arcs contained within over a user specified image. Although the choice of image is open, map and satellite data are recommended. 

This script is intended for use with latitude data obtained from [https://www.google.com/takeout/](https://www.google.com/takeout/)‎ and converted to kml using the [latitude-json-converter](https://github.com/Scarygami/latitude-json-converter) created by [Gerwin Sturm](https://github.com/Scarygami) and [Kyle Krafka](https://github.com/kjkjava).

## Usage

This script requires the Python Imaging Library (PIL) to run - please obtain from www.pythonware.com/products/pil/

Simply run the LatitudePlot.py file inside of a directory containing:

- All kml files to be rendered
- An image file for the kml arcs to be plotted on
- A csv file named ImageData.csv containing the following fields (in this order): image file name,top edge latitude,bottom edge latitude,left edge longitude,right edge longitude,(optional)x coordinate nudge,(optional)y coordinate nudge

Upon completion, an output file should be created in the directory named LatitudeData.png

Examples of use are at [my personal website](http://snowdonjames.com/rendering-long-term-location-data-from-google-latitude/)

## Example csv format:

For use with http://i.imgur.com/7pZFD7s.jpg (Southern United Kingdom)

    7pZFD7s.jpg,52.939176, 49.031686, -5.894165, 0.453186,-30,-5
    
or

for use with http://i.imgur.com/CjyohmR.jpg (whole United Kingdom)

    CjyohmR.jpg,59.925110, 48.892321, -11.096191, 1.944580,-2,10


This tool helps with finding the latitude and longitude of image corners: http://itouchmap.com/latlong.html 
