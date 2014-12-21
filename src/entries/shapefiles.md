title: shapefiles
created: December 20, 2014
blurb: messing with block-level census data
tags:
    - python

---

some basics on shapefiles:

* [wikipedia](http://en.wikipedia.org/wiki/Shapefile) has a nice intro
* .shp, .shx and .dbf files are required --
they're binary files with all of the vector data, indexing info and feature notes
* other optional files may be present too, like .prj (projection info)
* everything's sequential -- first record in the .shp corresponds to the first record in the .dbf
* fiona is a nice python package for reading shapefile info --
it returns [GeoJSON](http://geojson.org/geojson-spec.html#introduction)

* and here's a [gist](https://gist.github.com/yosemitebandit/335480129c103b91a0ba)
on using 2010 TIGER block-level census data to find the population of a circular area
