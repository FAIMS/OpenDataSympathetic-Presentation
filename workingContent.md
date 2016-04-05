# Instructions 

Authors are kindly asked to prepare one presentation file fulfilling both needs, the introductory 2-minutes-madness as well as the following intensive viewing and discussions. Please include the summary of your work in the first two slides followed by an unlimited number of slides going more into detail. The touch screens have a size of 42". The operating system is Windows 7 and they have internet access. Although the screens are in the 16:9 widescreen format, we recommend producing Power Point or PDF presentations in the classic 4:3 format. The extra space is used for the branding of the contribution as well as the navigation. The touch screens show three buttons allowing you to move forwards and backwards in the presentation as well as to access the table of contents (PICO programme) of that particular session. Please note that Prezi is not supported.

PICO is short, precise, and scientific. PICO is bringing the advantages of both, oral and poster, together into an innovative type of presentation which opens the opportunity to be interactive. Every PICO author presents first his/her work orally. But afterwards, all session attendees have enough time to watch the presentation again, to hold discussions with the author and colleagues, and to network.

A PICO presentation might be a Power Point one, a movie, an animation, or simply a PDF showing your research on a display. A PICO session takes place at the PICO spot which is a combination of an audience sitting in front of a screen together with a number of touch screen displays (PICO screens). The PICO session starts with a 2-minutes-madness, where all authors present the essence of their work in 2 minutes each. Thereby, time is reserved for one PICO presentation to provide a 10-minutes-introduction. Afterwards, the audience is using the PICO screens spread in the PICO spot to view again their PICO presentation(s) of interest. Authors are standing next to their scheduled screen to show their PICO presentation. A PICO presentation should be composed in a way to fulfil both requirements in one file, the 2 minute overview as well as the extensive viewing afterwards. To give you an idea how your PICO could look like please see the examples from the past conferences below:


# Abstract

Multiple people creating data in the field poses a hard technical problem: our “web 2.0” environment presumes constant connectivity, data “authority” held by centralised servers, and sees mobile devices as tools for presentation rather than tools for origination. A particular design challenge is the remoteness of the sampling locations, hundreds of kilometres away from network access. The alternative, however, is hand collection with a lengthy, error prone, and expensive digitisation process. 

This poster will present a field-tested[^footnote1] open-source solution to field data recording. This solution, originally created by a community of archaeologists, needed to accommodate diverse recording methodologies. The community could not agree on standard vocabularies, workflows, attributes, or methodologies, but most agreed that “recording data in the field’’ was a desireable app to have. As a result, the app is generalised for field data collection; not only can it record a range of data types, but it is deeply customisable. 

The NeCTAR funded FAIMS Project, therefore, created an app which allows for arbitrary data collection in the field[^footnote2]. In order to accomplish this ambitious goal, FAIMS relied heavily on OSS projects including: spatialite and gdal (for GIS support), sqlite (for a lightweight key-attribute-value datastore), Javarosa and Beanshell (for UI and scripting), and the entire linux stack plus ruby for a server. 

Only by standing on the shoulders of giants, FAIMS was able to make a flexible and highly generalisable field data collection system that CSIRO geoscientists were able to customise to suit most of their completely unanticipated needs[^footnote3]. While single-task apps (i.e. those commissioned by structural geologists to take strikes and dips) will excel in their domains, other geoscientists (palaeoecologists, palaeontologists, anyone taking samples), likely cannot afford to commission domain- and methodology- specific recording tools for their custom recording needs. FAIMS shows the utility of OSS software development and provides geoscientists a way forward for edge-case field data collection. Moreover, as the data is completely open and exports are scriptable, federation with other data formats is both encouraged and possible. 

This poster will describe the internal architecture of the FAIMS app, show how it was used by CSIRO in the field, and display a graph of its OSS heritage. The app is available from Google Play, the recording module can be found at https://github.com/FAIMS/CSIRO-Water-Samples and the exporter we used can be found at https://github.com/FAIMS/shapefileExport. You can make your own data-collection modules for free via the user to developer documentation at https://www.fedarch.org/support/2.


# Title Slide

Intent of slide: captioned visual narrative. This slide can be used to describe the complete workflow of module history, generation, and use

Grid of pictures: 

## Cell 1
![Geosampling data was initially collected via notebook.](noteBook1.jpg)

Caption: Geosampling data was initially collected via notebook.

## Cell 2

![Simplied via pre-printed Field Data Book](noteBook2.jpg) ![With labels for more accurate entry](noteBook3.jpg) 
Combined image caption: CSIRO Researchers then moved to pre-printed field notebooks for more accurate data entry. 

## Cell 3
![CSIROWireframe.pdf](CSIROWireframe.png)
Caption: Imported into FAIMS Mobile. CSIRO workflow modeled in the generalised field recording app. Once approved, this workflow was implemented.


## Cell 4

Data Schema | Logic | UI Schema |
----------- | ----- | --------- | 
![dataSchema.png](dataSchema.png) | ![uiLogic.png](uiLogic.png) | ![uiSchema.png](uiSchema.png) | 

 Caption: Available at https://github.com/FAIMS/CSIRO-Geochemistry-Sampling. These are the primary files which implement a scriptable model (data schema) | view (ui schema) | and controlller (ui logic) field data recording implementation. By scripting a field recording workflow, the app itself can function on supporting field recording in network-degraded environments, and individual "modules" (functioning sets of these scripts) can focus on implementing highly specific and customised workflows. | 

## Cell 5

![1.png](app1.png) | ![2.png](app2.png) | ![3.png](app3.png) 
----------- | -------- | --------- 

Caption: After extensive testing, an app was deployed. These are three screens, designated by the wireframe and scripted by the files before.

## Cell 6

![field](establishingShot.jpg)
Caption: Data was collected on multiple tablets in the field

## Cell 7
![truck](faimsInTruck.jpg) 
Caption: FAIMS is designed to work completely offline, allowing asynchronous work on multiple tablets with eventual sync. The server, here, was built into a portable UPS in the truck.

## Cell 8
![export](export.png) | ![exportData](exportData.png)
Caption: After return to base, data exported (via customisable exporter) into shapefiles, a sqlite database, and CSVs. All pictures are renamed to the record they belong to and tagged with their record's meta-data. This exporter (https://github.com/FAIMS/shapefileExport) is also completely customisable, up to and including running arbitrary linux programs. This one uses imagemagick and mogrify to properly export photos as well as spatialite-tool to export shapefiles. 


## Bottom Discussion

FAIMS Mobile is a FOSS Software platform (comprising an android client and ruby server on ubuntu) funded by the Australian Research Council designed to provide a means of collecting rich, geospatial, and multi-media field data on multiple tablets with no network connectivity in the middle of nowhere. While originally intended to support archaeologists, FAIMS Mobile provided a sufficiently general field recording framework to allow for geochemical and biological sampling by multiple teams of CSIRO researchers.

Code for this module is available at: https://github.com/FAIMS/CSIRO-Geochemistry-Sampling. The module can be explored by downloading FAIMS from google play and downloading the *CSIRO Geochemical Sample Collection - Sydney Maps* module from the demo server. A getting started guide is available at: http://faims.edu.au


Paper notes: 

# Detail Slide

Intent of slide: Faims internal architecture, OSS Heritage graph

# Supplimentary Slides

## CSIRO Workflow

## Module Details

## Faims internal architecture

## OSS Heritage graph
