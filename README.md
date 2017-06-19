# World Heritage Analyses

[The World Heritage Analyses](https://yichuans.github.io/wh-knowledge-lab/) is a digital lab (hereafter referred to as the Lab) by the [IUCN World Heritage Programme](https://www.iucn.org/theme/world-heritage/) to utilise the power of the web to effectively deliver data, information and knowledge on natural World Heritage sites. 

## Index of prototypes
- [Land Cover Change](#1-land-cover-change)
- [Forest loss and Human footprint](#2-forest-loss-and-human-footprint)
- [Species Climate change vulnerability](#3-climate-change-and-species-vulnerability)
- [Near real time Landsat 8 imagery](#4-near-real-time-landsat-8-imagery)
- [World Heritage boundary](#5-world-heritage-boundary)
- [Global spatial comparative analysis](#6-global-spatial-comparative-analysis)
- [World Heritage information sheet](#7-world-heritage-information-sheet)
- [Global surface water transition](#8-global-surface-water-transition-on-google-earth-engine)

## About

We care deeply about the well-being of our rich natural heritage, which have increasingly become under accelerating threats. More rapid, accessible and easily digestible digital information, in particular through the provision of GIS and remote sensing, is urgently required to broaden our understanding as well as to inform better decision making. 

Digital products are increasingly becoming the *de facto* preferred means through which the public access information. Rather than producing papers and publications that are difficult to understand and time consuming to read, we want to better connect with our audience by improving user experience.

With little resources, we need to keep things simple, but focus on the most important part, one at a time. We try our best to make one thing work, and hopefully to make one thing work well without investing much time. This is only achievable because we stand on the shoulders of giants and benefit from those who have gone there and have done all the hard work, already. For example, our near-real time satellite images for natural sites rely on esri's [Landsat Image Service](https://www.arcgis.com/home/item.html?id=3f26216ee3a54f138e940aa1b4638eb5), the analyses of forest loss and human footprint are derivative works based on research by the [Hansen forest loss data](http://data.globalforestwatch.org/datasets/63f9425c45404c36a23495ed7bef1314), and [Human footprint data](http://wcshumanfootprint.org/) by the University Queensland and Wildlife Conservation Society.

We believe in the principle of open data, and an open source approach, so everything we do can be easily reproduced, scrutinised, and extended with absolute freedom. This is the future, and we owe our thanks much to those who inspire us to head this way.

More specifically the Lab aims to be:

- A central hub where all proof-of-concept ideas and work-in-progress projects, ideas of small and big, are tried, tested and presented.

- An entry point to access data, analyses, findings, and prototype tools, 

- A mechanism to gather feedbacks to engage users, whom we rely on to guide us in the right direction so we deliver data, information and knowledge that are **useful** and **fit for purpose**.

## The Lab itself

This page also hosts the source code behind the World Heritage Analyses itself, with the design inspired by [Start Bootstrap](http://startbootstrap.com/), [Stylish Portfolio](http://startbootstrap.com/template-overviews/stylish-portfolio/)

# Prototypes

Here we present a collection of studies, analyses and prototype tools that have been, or are being, developed using affordable technology, existing scientific research and data products to provide perspectives for natural World Heritage sites. We hope by sharing these work-in-progress as soon as possible through the web, so we are able to listen to you, accommodate your thoughts, mobilise resources, and to ensure effort is only spent on things that are useful.

## 1. Land cover change

### Innovation

The first comprehensive land class mapping exercise for all natural World Heritage sites and their change over time. It is also the first time the web was used to deliver the findings, instead of a text heavy report. The result has the potential in identifying threats manifested as change in land cover.

### About

Accurate global land cover remains a well-known challenge, let alone comparable land cover change over time. Notable global land cover data products include the Global Land Cover for the year 2000 (GLC2000) at 1km spatial resolution, European Space Agency's (ESA) GlobCover 2009 at 300m resolution, more recently the [GlobalLand30](http://www.globallandcover.com) land cover datasets represent the potential to enable comparisons to be made at the site level globally, for natural World Heritage sites, between 2000 and 2010.

We analysed based each land cover pixel in 2000 and 2010 for each natural World Heritage site and tracked their transition. For example, a pixel identified as forest in 2000 and then the same pixel was then classified as grassland. By aggregating the number of these pixels and the area they represent, we were able to derive not only the total area of each land cover class, but also estimate the conversion between land cover classes.

As with any results derived from global analyses, despite the nature of consistency, the finding may not capture every detailed difference. Additionally the result may also reflect the varied quality and accuracy of the underlying land cover data, which are dependent on the characteristics of the samples and methodology used in the classification. These are beyond the control of our work here. One further caveat is that although it is possible to quantify the extent and change of land covers, the reason behind the observed change requires further interrogation, ideally with the support of auxiliary information or expert systems. For example, the change of forest to grassland may be anthropogenic, such as a result of clearing for grazing; or it could be due to fire, a natural disturbance in ecological successions. While it is not advisable to use the finding of this study to directly inform monitoring *per se*, it could be used as an independent source of information to identify areas that may merit further investigation, as part of an early warning system.

- Result: GlobeLand30 data 2000-2010, for all natural sites up to 2015. 10 classes change matrix (sankey diagram visualisation) on the web portal to easily visualise trend of change.
- Issues: results not validated with unquantified quality and accuracy across the world
- Tech stack: Python (arcpy and numpy), GDAL, Web2py, Bootstrap, jQuery, D3js, D3js-Sankey plugin, leaflet. Data courtesy of National Geomatics Centre of China.

[Land cover change website](http://wh-app.yichuans.me/wh_app/landcover) | [Source on Github](https://github.com/Yichuans/World_Heritage_apps)

## 2. Forest Loss and Human Footprint

### Innovation

The first exercise of amplifying the impact of findings of peer-reviewed journal papers by complementing with web based portals for site specific information. We hope by doing so we overcome the barrier of inaccessible science (be it too difficult to understand or simply unwieldy in real life use) and project useful information directly to the hands of those who may actually use them. We also attempted for the first time a comment system as a way of channelling user feedback and also to encourage discussion and debate, to further enhance our own understanding, for example, in understanding the *reason* for the observed change in forest and human footprint.

### About

Accompanying the [forest loss and human footprint paper on natural World Heritage Heritage](http://www.sciencedirect.com/science/article/pii/S0006320716310138), they hold site specific information that can be of use to practitioners on the ground, as well as a means through which to verify results and gain site level insight beyond information from a global data driven approach. The site specific information is not published in the paper, in which only global statistics are given.


- Result: Derived work from [Hansen forest loss data](http://data.globalforestwatch.org/datasets/63f9425c45404c36a23495ed7bef1314), and [Human footprint data](http://wcshumanfootprint.org/) by the University Queensland and Wildlife Conservation Society; quantitative breakdowns and with maps, to track change over time.
- Issues: only forest loss but not deforestation; no distinction between primary forest and plantation; change may be a result natural process (for example habitat succession), and it is not without difficulty in interpreting the result with contextual information and on the ground knowledge.
- Tech stack: Pelican, Bootstrap, Disqus comments.

[Forest Loss](http://world-heritage-analyses.greenfirescience.com/forest-loss/) | [Source on Github](https://github.com/Yichuans/forest-loss)

[Human Footprint Change](http://world-heritage-analyses.greenfirescience.com/human-footprint/) | [Source on Github](https://github.com/Yichuans/human-footprint)

## 3. Climate change and species vulnerability

### Innovation

The first data analytics exercise involving version control, open, accessible, reproducible methods. It represents a brand new way of analysing data, delivering results, and communicating knowledge products, throughout its life cycle from inception to deployment, embodying a good example of the digital by default approach. The result can be replicated step by step (see below links for detail), provided the same data is used. This open approach enables interested users to both critique the methodology as it is completely transparent to the every detail, and also further work to improve the analysis, collaboratively. 

The extensive use of charts and graphs that replace narrative explanations makes it easier and simpler for users to access findings. 

### About

This work is based on a global study on species climate change vulnerability (Foden 2012, see below link).

Species vulnerability results were transferred to sites based on the spatial relationship between RedList species and natural World Heritage boundaries, using a sensitivity tested overlap threshold. As a well known caveat, the Extent of Occurrence (EOO) range polygons in the IUCN RedList database is a poor estimate of true species distribution with unaccounted omission and commission errors, nevertheless, they remain the only globally consistent data from comprehensive assessments.

By summing the number of climate change vulnerable species by their Sensitivity, Low Adaptability and Exposure scores, we are able to obtain a climate vulnerability assessment from the point of view of species for each natural World Heritage site. Since the scores are relative within each comprehensively assessed taxon, we conducted the analysis by treating amphibians, birds and warm water reef building corals separately. Furthermore, the aggregates statistics uncovered each trait and exposure detail and such information may be most relevant and useful to specific climate change adaptation monitoring requirement and policies on mitigation. As a result, users will be able to derive information such as: the prevalent cases of low adaptability is due to long generation length for a number of birds.

- Result: Derived work from [Foden 2012](http://journals.plos.org/plosone/article?id=10.1371/journal.pone.0065427). Entirely open, including data, method and results and reports, all of which are available online
- Issues: review process is complicated for those not familiar with a version control system such as Github.
- Tech stack: web2py, JSON service-based for future extendibility, D3js

[Climate change vulnerability](http://wh-app.yichuans.me/ccv) | [methodology](http://nbviewer.jupyter.org/github/Yichuans/climate-vulnerable-wh/blob/master/workspace.ipynb) and [report](http://nbviewer.jupyter.org/github/Yichuans/climate-vulnerable-wh/blob/master/report.ipynb) | [Source on Github](https://github.com/Yichuans/climate-vulnerable-wh)

## 4. Near real-time Landsat 8 imagery 

### Innovation

The first application built on external web services (esri's Image Services). This is a significant step forward: by doing so, we free ourselves from the laborious, difficult, expensive, and non essential tasks of tracking Landsat 8 imagery as they become available, downloading and processing images, and uploading them to a web based portal for viewing. This results in an end product which can then focus on presenting Landsat 8 images, in near real time, for natural World Heritage that self updates and requires no maintenance and little computation power.

This is the also the first time that remote sensing images (Landsat 8) are collated for all natural World Heritage sites at near real time.

### About

This application evolved from a pilot study implementing a custom built system that tracks an online catalogue of Landsat 8 images on [Amazon](https://aws.amazon.com/public-datasets/landsat/), for a small number of natural World Heritage sites. The system automatically downloads new images when they become available and if they meet certain quality criteria. Then, scheduled tasks are carried out to process the images, such as pre-processing, band combinations and pan-sharpening, and finally updates an internal database and archives for future use. The vision of using these archived imagery, such as visualising on the web, was a remote goal, as significant resources and infrastructure are required.

As a proof of concept, time series Landsat 8 images are now displayed in juxtaposition to allow visual interpretation of change over time. This is aided by the functionality of dynamically changing band combinations on the fly. The flexibility of the image services means that any time sequence can be selected and visualised easily - a sustainable way to expand functionality without major re-engineering. 

The benefits of rear real time satellite images are multitude. An obvious one is the possibility of 'seeing' World Heritage sites from space, back in time and also present, some of which remain inaccessible due to their remote location and hugely vast size. This could help experts with significant experience on the ground to scale up their knowledge and apply across the site. It also enables large scale analysis, previously unavailable or expensive, to generate new insights, for example, in identifying possible threats such as long term land cover conversion trend, or in detecting disturbances such as fire. 

It is worth noting that, despite their vast potential, they do not replace the need for ground based surveys and monitoring missions well established in statutory process, due to limitations such as resolution and the subsequent difficulty of high fidelity analysis. Like land cover change, it may be possible in the future to eventually detect every change in pin-point accuracy, however, it will not explain the reason why by itself alone.

- Result: Using time series data for WH with near-real time monitoring, in a more accessible and timely way.
- Issue: relies on external Landsat services, currently for views only and very limited analytical function, for example dynamic band combination.
- Tech stack: esri web services and esri calcite framework

[Landsat 8 imagery for natural World Heritage](http://wh-app.yichuans.me/landsat) | [Source on Github](https://github.com/Yichuans/landsat)

## 5. World Heritage Boundary

### Innovation

The natural World Heritage Boundary is now a data service that everyone can download, visualise and integrate in their own work

### About

The natural World Heritage boundary evolved from a KML file with patchy point and polygons (the very original came from the UNESCO World Heritage Centre). In 2011-2012, a major overhaul was commissioned that saw significantly improved data quality, with more than three quarters of the boundaries corrected, replaced, updated or completely re-mapped, in cases where boundaries were reverse-engineered from large scale paper maps. Since then, IUCN continues to invest in the dataset, by incorporating newly inscribed natural sites, and by ensuring the best available boundary is included in the database. This data is also part of the World Database on Protected Areas (WDPA). 

Spatially explicit boundary is a fundamental requirement when it comes to protected area evaluation and effective monitoring, especially in the context of natural World Heritage Convention. The Outstanding Universal Values, which underpin the World Heritage status, requires a well defined geographical boundary, without which no assessment could be made on value justification, protection and management nor integrity requirements. A comprehensive and accurate database of these boundaries allows scientifically robust scrutiny of the distribution of natural sites, their comparative representation and irreplaceability, crucially important for the credibility of the Convention. Unfortunately the Convention does not require the submission of GIS data as a requirement for the nomination, albeit the technology has been unanimously adopted and widely used.

In term of monitoring and policy guidance, most large extractive companies have pledged that no active operation nor exploration should take place within natural World Heritage sites. Having a GIS boundary facilitate that understanding and leaves no room for ambiguity. World Heritage boundaries have supported many scientific and research initiatives, including the [World Heritage Outlook](http://www.worldheritageoutlook.iucn.org), [Thematic Studies](https://www.iucn.org/theme/world-heritage/resources/publications), and [World Heritage and benefits](https://www.iucn.org/theme/world-heritage/our-work/world-heritage-projects/benefits-natural-world-heritage), to name a few.

Please see below for various links to the boundary (no commercial use and no re-distribution).

[Natural World Heritage Viewer](http://wcmc.io/3f3e) | [esri Feature Service](http://www.arcgis.com/home/item.html?id=d40e5b2b9be843ddb03eefb04c173ca4) | [REST end point](http://services5.arcgis.com/Mj0hjvkNtV7NRhA7/arcgis/rest/services/Latest_WH/FeatureServer)

## 6. Global spatial comparative analysis

### Innovation


### About


[Comparative analysis](http://whca.yichuans.me/) | [Source on Github](https://github.com/Yichuans/comparative-analysis-online)

## 7. World Heritage information sheet

### Innovation


### About

[Information sheet](https://yichuans.github.io/datasheet/output/) | [Source on Github](https://github.com/Yichuans/datasheet)

## 8. Global surface water transition on Google Earth Engine

### Innovation


### About
