---
layout: post
title: Automated classification metrics for energy modelling of residential buildings in the UK with open algorithms
---

We have a new [journal article](http://journals.sagepub.com/eprint/h489ZksJJ9RKMEbFYNRj/full) on using [Ordnance Survey MasterMap](https://www.ordnancesurvey.co.uk/business-and-government/products/topography-layer.html) and [AddressBase Plus](https://www.ordnancesurvey.co.uk/business-and-government/products/addressbase-plus.html) data for energy modelling studies published in Environment and Planning B: Urban Analytics and City Science. The paper describes techniques to automatically extract information on the geometric and topological characteristics of residential buildings, which can then be used as parameters for estimating the energy use at the city scale. 

We describe creating a spatial database of residential properties, qualitative classification of each building's form according to its spatial relations, and the addition of quantitative metrics relating to the building envelope. The techniques described in the article were implemented as [PostGIS](https://postgis.net/) database queries and have been made available at [pgBuiltForm](https://github.com/lucas-uk/pgBuiltForm) under a Creative Commons Attribution 4.0 licence.

Abstract:
>*Estimating residential building energy use across large spatial extents is vital for identifying and testing effective strategies to reduce carbon emissions and improve urban sustainability. This task is underpinned by the availability of accurate models of building stock from which appropriate parameters may be extracted. For example, the form of a building, such as whether it is detached, semi-detached, terraced etc. and its shape may be used as part of a typology for defining its likely energy use. When these details are combined with information on building construction materials or glazing ratio, it can be used to infer the heat transfer characteristics of different properties. However, these data are not readily available for energy modelling or urban simulation. Although this is not a problem when the geographic scope corresponds to a small area and can be hand-collected, such manual approaches cannot be easily applied at the city or national scale. In this article, we demonstrate an approach that can automatically extract this information at the city scale using off-the-shelf products supplied by a National Mapping Agency. We present two novel techniques to create this knowledge directly from input geometry. The first technique is used to identify built form based upon the physical relationships between buildings. The second technique is used to determine a more refined internal/external wall measurement and ratio. The second technique has greater metric accuracy and can also be used to address problems identified in extracting the built form. A case study is presented for the City of Nottingham in the United Kingdom using two data products provided by the Ordnance Survey of Great Britain: MasterMap and AddressBase. This is followed by a discussion of a new categorisation approach for housing form for urban energy assessment.*


The full paper is available at: [http://journals.sagepub.com/eprint/h489ZksJJ9RKMEbFYNRj/full](http://journals.sagepub.com/eprint/h489ZksJJ9RKMEbFYNRj/full)

The code is available on Github: [pgBuiltForm](https://github.com/lucas-uk/pgBuiltForm) 