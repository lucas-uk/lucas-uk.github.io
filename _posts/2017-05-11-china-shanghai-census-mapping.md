---
layout: post
title: Mapping migration data for China and Shanghai
---
*Written by [Stephen Parkes](https://www.nottingham.ac.uk/geography/people/stephen.parkes) and [Julian Rosser](http://www.nottingham.ac.uk/engineering/people/julian.rosser)*

Migration within China has accelerated rapidly in recent decades, a characteristic of the substantial expansion of the country’s economy and the growing demand for urban living. As part of our work studying Shanghai we have been examining the patterns of migration to the city, based on data available through the 2010 national census. 
 
This work was conducted by Shuang Hu - a PhD student connected to [LUCAS](http://www.nottingham.ac.uk/research/groups/lucas/index.aspx) – and was motivated by a desire to capture the flow of migrants to Shanghai and their reasons for moving, where they locate within the city, and what this might mean for the city socially, environmentally, and economically. The data on migrations includes all those individuals who have migrated up to 2010, not just in the past year, for example.

As part of this work, we have been creating maps of migration for China and Shanghai using the [Leaflet](https://rstudio.github.io/leaflet/) and [R](https://www.r-project.org/). 

## Migration into Shanghai
 
The first map shows the origins of interprovincial migrants in Shanghai. It is clear here that geographic distance appears to act as one of the determinants for locating to Shanghai. The highest volumes of migrants originate from the provinces closest to Shanghai (e.g. Anhui and Jiangsu), whilst far fewer migrants are drawn from the provinces to the west of China. 


<div class="iframe-container">
    <iframe src="https://lucas-uk.github.io/shanghaiR/numbersOfChinaMigrantsToShanghai.html" height="315" width="560" allowfullscreen="" frameborder="0">
    </iframe>
</div>
[Fullscreen map](https://lucas-uk.github.io/shanghaiR/numbersOfChinaMigrantsToShanghai.html)


The boundaries, base data and migration figures for the map have been taken from [GADM](http://gadm.org/) database, [OpenStreetMap](http://openstreetmap.org) respectively and [census data](http://www.stats-sh.gov.cn/data/toTjnj.xhtml?y=2010) . 

## Location of migrants within Shanghai

In the second map we observe where within the city boundary the migrants have located. The districts with the highest densities of migrants per km2 are located more centrally (e.g. Hongkou and Huangpu). The highest volumes of migrants per district however are located to the south (in Minhang, Songjiang, and Pudong). 


<div class="iframe-container">
    <iframe src="https://lucas-uk.github.io/shanghaiR/shanghaiMigrantsDensityMap.html" height="315" width="560" allowfullscreen="" frameborder="0">
    </iframe>
</div>
[Fullscreen map](https://lucas-uk.github.io/shanghaiR/shanghaiMigrantsDensityMap.html)


The extract of [census data](http://www.stats-sh.gov.cn/data/toTjnj.xhtml?y=2010) used for mapping migration was for 2010, and since the Shanghai district boundaries have changed since that time the current data available from GADM was unsuitable for the city scale mapping. To try and address this, we extracted 2010 data of [OpenStreetMap](https://openstreetmap.org) using the contribution history drawn from the [OSM planet database](https://planet.openstreetmap.org/planet/full-history/). However, a clear lack of quality OSM contributions in 2010 was apparent with the geometry of many districts seen to be incomplete. Thus, OSM 2014 boundary data was adopted with certain district migration counts merged to create values consistent with the more recent mapping.

The code for creating both these maps is available from the [LUCAS github](https://github.com/lucas-uk/) repository: [China / Shanghai migration in R](https://github.com/lucas-uk/shanghaiR).

Further insights from this data analysis will feature in a future blog post. In the meantime, any queries can be directed to [Julian Rosser](http://www.nottingham.ac.uk/engineering/people/julian.rosser) (mapping) or [Stephen Parkes](https://www.nottingham.ac.uk/geography/people/stephen.parkes) (migration). 

