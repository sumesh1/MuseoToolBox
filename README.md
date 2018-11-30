![MuseoToolBox logo](https://github.com/lennepkade/MuseoToolBox/raw/master/metadata/museoToolBox_logo_128.png)

**Museo ToolBox** is a python library to simplify the use of raster/vector. One of the most important contributions is the interface between a cross-validation strategy and learning/predicting with Scikit-Learn. 

The other meaningful contribution is the **rasterMath** function which allow you to do whatever you like on a raster in a few lines : mean/modal/prediction/whittaker (you use your own function), and **rasterMath** manage everything : the nodata value, reading the raster block per block, saving to a new raster...

## Who build Museo ToolBox ?
I am [Nicolas Karasiak](http://www.karasiak.net), a Phd student at Dynafor Lab. I work on the identification of tree species throught dense satellite image time series, especially with Sentinel-2. A special thanks goes to [Mathieu Fauvel](http://fauvel.mathieu.free.fr/) who gave me the love of good and open-source coding.

## What's the point ?
Today, the main usages of Museo ToolBox are :
- **crossValidationsTools**
  - Create validation/training sets from vector, and Cross-Validation directly compatible with Scikit-Learn GridSearchCV. The aim is here to **promote the spatial validation/training** in order to lower spatial auto-correlation.
- **rasterTools**
  - Extract band value from vector ROI (polygons/points)
  - **rasterMath**, certainly the most useful for most of the users : allows you to do some math on your raster. Just load it, rasterMath will return you the value for each pixel (in all bands) and do whatever you want : predicting a model, signal treatment (whittaker, double logistic...), modal value, mean...
- **learnTools**
  - Based on Scikit-Learn. Allow to use the cross-Validations from Museo ToolBox or from Scikit-Learn and to extract each kappa/confusion matrix from fold. Ease the way to predict a raster (just give the raster and the classification file to save and Museo will do everything).

## That seems cool, but is there some help to use this ?
I imagined Museo ToolBox as a tool to promote the use of spatial cross-validation (or validation/training at least by subgroup) and to learn and predict from raster, so of cours I gave a lot of examples : [a complete documentation with a lot of examples is available on readthedocs](https://museotoolbox.readthedocs.org/).

## How do I install it ?
A package will be available on pip : 
`python3 -m pip install MuseoToolBox` 

## Why this name ?
As Orfeo ToolBox is one my favorite and most useful library to work with raster data, I choose to name my work as Museo because in ancient Greek religion and myth, [Museo is the son and disciple of Orfeo](https://it.wikipedia.org/wiki/Museo_(autore_mitico)). If you want an acronym, let's say MUSEO means 'Multiple Useful Services for Earth Observation'.
