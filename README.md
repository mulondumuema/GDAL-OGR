# about GDAL

The Geospatial Data Abstraction Library (GDAL) is a computer software library for reading and writing raster and vector geospatial data formats, and is released under the permissive X/MIT style free software license by the Open Source Geospatial Foundation. As a library, it presents a single abstract data model to the calling application for all supported formats. It may also be built with a variety of useful command line interface utilities for data translation and processing. Projections and transformations are supported by the PROJ library.

The related OGR library (OGR Simple Features Library), which is part of the GDAL source tree, provides a similar ability for simple features vector graphics data.


You can visit the [GDAL Website](https://gdal.org/programs/index.html).

For example:

```gdal_info <raster-dataset>``` is for listing information about a raster dataset

```gdal_translate ...``` converts raster data between different formarts

```gdaldem``` analyse and visualize DEMs

You can use the softwares for viewing

Will use gdal with bash, e.g to list all tiff files:

```ls *.tif```

you can us the the gdal_info command as above to view more details of a specific file

to check minimum and maximum, you can write:

```gdalinfo -mm <raster_dataset>```

Understanding data type

This explains the data type to save your data depending on the range of values in the dataset. For example an aerial imagery with RGB values ranging fron 0 to 255 will be saved as byte while for a dem, you will save it depending on the range of its values.

creating the index shapefile:

```gdaltindex tile_index/ecw_index.shp *.ecw```

```gdaltindex -t_srs EPSG:4326 -src_srs_name src_srs tile_index/ecw_srs_index.shp *.ecw```

