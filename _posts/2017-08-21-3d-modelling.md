---
layout: post
title: Urban energy modelling using CityGML
---
Written by [Julian Rosser](http://www.nottingham.ac.uk/engineering/people/julian.rosser)

On the [Sustaining Urban Habitats](http://www.nottingham.ac.uk/research/groups/lucas/research/sustaining-urban-habitats-an-interdisciplinary-approach.aspx) project, part of our work is focused on predicting building energy use so that measures for reducing energy demand may be effectively targeted. Simulation requires representative 3D city models of urban areas so that accurate estimates of energy demand imposed on the city can be made. 

Over the last years, 3D city models have become increasingly common. [CityGML](https://www.citygml.org/) has emerged as a standardised representation of the shape and features that make up urban areas. This [Open Geospatial Consortium](http://www.opengeospatial.org) standard uses the concept of Levels of Detail to categorise the complexity and amount of information present in the urban scene. The classification reflects both the geometry and semantics of the objects contained within the model.  

<p align="center">
Example CityGML 3D model view at Levels of Detail 1 -4 (needs HTML5)
</p>
<div class="iframe-container">
    <iframe src="https://lucas-uk.github.io/WebGL-model-demo/Apps/model_lod.html" height="315" width="560" allowfullscreen="" frameborder="0">
    </iframe>
</div>
[Fullscreen model viewer](https://lucas-uk.github.io/WebGL-model-demo/Apps/model_lod.html)

Despite steady improvements in aerial surveying procedures creating 3D data (e.g. LiDAR, photogrammetry), many applications still start with 2D geospatial data as a base (e.g. either [OpenStreetMap](https://www.openstreetmap.org) or map data from a national provider, like [Ordnance Survey](http://www.ordnancesurvey.co.uk)). The building footprints are then transformed, perhaps using an extrusion, geometric modelling (such as a triangulation) or procedural modelling, to add in 3D detail. To create CityGML models at LOD2 or above, these buildings models then must be processed such that particular components are correctly attributed e.g. as RoofSurface, GroundSurface and WallSurfaces. At LODs 3 and 4, components such as windows, doors and rooms may be included.

Application Domain Extensions (ADE) allow additional domain specific details to be added to the model. In the case of energy modelling and simulation, the [EnergyADE](http://www.citygmlwiki.org/index.php/CityGML_Energy_ADE) produced by [SIG3D](http://www.sig3d.de/) is particularly relevant. This allows for inclusion of attributes on energy efficiency, thermal properties, construction materials and so forth. Example CityGML and EnergyADE models can be found on the web, however, relatively few for the UK are readily available. As such we've created some sample models of our office building using OpenStreetMap and [UK Environment Agency open LiDAR](https://data.gov.uk/dataset/lidar-composite-dsm-1m1) at LOD2, and mapped in some EnergyADE attributes according to the [v0.6 schema](https://github.com/cstb/citygml-energy). 

[Sample CityGML building](https://lucas-uk.github.io/public/Lenton_Hurst_OSM_CityGML.xml)

[Sample CityGML building with EnergyADE attributes](https://lucas-uk.github.io/public/Lenton_Hurst_OSM_CityGML_EnergyADE.xml)
