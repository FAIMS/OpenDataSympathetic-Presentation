Working repo for: EGU2016-13182
Using the FAIMS Mobile App for field data recording
by Brian Ballsun-Stanton et al.
accepted in Session ESSI3.5/GI1.5 Free and Open Source Software (FOSS) for Geoinformatics and Geosciences (co-organized) # Using the FAIMS Mobile App for field data recording Brian Ballsun-Stanton (1), Jens Klump (2), and Shawn Ross (1) (1) FAIMS Project, Macquarie University, Sydney, Australia (brian.ballsun-stanton@mq.edu.au), (2) CSIRO Mineral Resources, CSIRO, Bentley, Australia (Jens.Klump@csiro.au) 

Multiple people creating data in the field poses a hard technical problem: our “web 2.0” environment presumes constant connectivity, data “authority” held by centralised servers, and sees mobile devices as tools for presentation rather than tools for origination. A particular design challenge is the remoteness of the sampling locations, hundreds of kilometres away from network access. The alternative, however, is hand collection with a lengthy, error prone, and expensive digitisation process. 

This poster will present a field-tested[^footnote1] open-source solution to field data recording. This solution, originally created by a community of archaeologists, needed to accommodate diverse recording methodologies. The community could not agree on standard vocabularies, workflows, attributes, or methodologies, but most agreed that “recording data in the field’’ was a desireable app to have. As a result, the app is generalised for field data collection; not only can it record a range of data types, but it is deeply customisable. 

The NeCTAR funded FAIMS Project, therefore, created an app which allows for arbitrary data collection in the field[^footnote2]. In order to accomplish this ambitious goal, FAIMS relied heavily on OSS projects including: spatialite and gdal (for GIS support), sqlite (for a lightweight key-attribute-value datastore), Javarosa and Beanshell (for UI and scripting), and the entire linux stack plus ruby for a server. 

Only by standing on the shoulders of giants, FAIMS was able to make a flexible and highly generalisable field data collection system that CSIRO geoscientists were able to customise to suit most of their completely unanticipated needs[^footnote3]. While single-task apps (i.e. those commissioned by structural geologists to take strikes and dips) will excel in their domains, other geoscientists (palaeoecologists, palaeontologists, anyone taking samples), likely cannot afford to commission domain- and methodology- specific recording tools for their custom recording needs. FAIMS shows the utility of OSS software development and provides geoscientists a way forward for edge-case field data collection. Moreover, as the data is completely open and exports are scriptable, federation with other data formats is both encouraged and possible. 

This poster will describe the internal architecture of the FAIMS app, show how it was used by CSIRO in the field, and display a graph of its OSS heritage. The app is available from Google Play, the recording module can be found at https://github.com/FAIMS/CSIRO-Water-Samples and the exporter we used can be found at https://github.com/FAIMS/shapefileExport. You can make your own data-collection modules for free via the user to developer documentation at https://www.fedarch.org/support/2.


[^footnote1]: See chapter by Sobotkova et. al. in forthcoming book Mobilizing the Past due out at the end of 2016

[^footnote2]: Ross, S., et. al. (2015). Building the bazaar: enhancing archaeological field recording through an open source approach. In Wilson, A. T., Edwards, B. (Eds.). Open Source Archaeology: Ethics and Practice. Walter de Gruyter GmbH Co KG.

[^footnote3]: Reid, N., et. al. (2015) A mobile app for geochemical field data acquisition. Poster session presented at the meeting of AGU Fall Meeting, San Francisco