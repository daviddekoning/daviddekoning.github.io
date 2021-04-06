---
layout: post
title: A list of Open Structural Analysis formats
---

The recent publication of the [ShapeDiver Transfer Format](https://github.com/shapediver/sdTF), 
got me thinking about data standards in AEC...again! My day job is leading
Arup's development and deployment of [Speckle](https://v1.speckle.systems)
and neutral data formats, particularly for structural analysis, are a recurring theme.

While everyone agrees that it would be wonderful for everyone to use a single, simple and open data format,
it is very hard to 1) find anyone willing to take a stab at creating a format that meets everyone's needs 
("BuildingSMART takes too long and doesn't produce anything useful!") or,
2) to convince anyone to contribute to an existing schema rather than creating a whole new one ("That standard
doesn't meet my specific needs - I need to write a new one!")

I haven't seen a list of open formats for structural engineering analysis, so I thought I would take a stab
at describing the current (and recent past) landscape of formats in play in the AEC industry. I've left out the
more academic focused open formats like [OpenSEES](https://opensees.berkeley.edu/).

[Let me know on twitter](https://twitter.com/intent/tweet?text=@ddkto%20you%20missed%20a%20format!) if I've missed
any other formats!

## [DesignLink](https://www.academia.edu/download/49070380/ad.110720160923-5864-1szd924.pdf)

This collaboration between [Arup](https://www.arup.com/) and the 
[Spatial Information Research Lab (SAIL)](http://www.sial.rmit.edu.au/) underpinned some tooling 
used within Arup, but never gained much traction in the wider industry. We do talk about open sourcing it
for posterity every now and then, but seem to always be busy with something else...

## [Speckle Structural](https://github.com/arup-group/SpeckleStructural)

Originally written by a brilliant intern, this open format is loosely based on the 
[Oasys GSA](https://www.oasys-software.com/products/structural/gsa/) file format. The interesting twist
is that it uses the [Speckle Core Geometry (v1)]() format to describe its geometry, which means that
programs that can read Speckle geometry (SpeckleRhino, SpeckleGH, etc...) can also ingest the geometry
of a strutural analysis model.

## [BHOM Structural](https://github.com/BHoM/BHoM/tree/master/Structure_oM)

Part of Buro Happold's [Building Habitat Object Model](https://bhom.xyz), this format is 
similar to Speckle Structural in that the  geometric entities inherit from generic geometric 
schema and so can be ingested by non-strutural design software.

## [Structural Analysis Format](https://saf.guide)

SAF is an initiative from the [Nemetschek Group](https://www.nemetschek.com/) to improve the collaboration between structural 
engineers by developing an open exchange format for exchanging data between structural 
analysis software based on the Excel format. Don't be put off by the fact that it is based on 
Excel - it is actually a nice and tidy relational data model, just as happy in a set of CSV files, an sqlite file
or a PostGreSQL database.

## [SkyCiv 3d Model](https://skyciv.com/api/v3/docs/s3d-model)

[SkyCiv](https://skyciv.com/) is an online structural analysis platform, and they publish their data format openly.

## [IFCStructuralAnalysisModel](https://standards.buildingsmart.org/IFC/RELEASE/IFC4_1/FINAL/HTML/schema/ifcstructuralanalysisdomain/lexical/ifcstructuralanalysismodel.htm)

I have not looked into this in great detail, but it appears to be used in [GeometryGym's IFC-based workflows](https://github.com/GeometryGym/GeometryGymIFC/blob/a6807578a53769cd02b96fb6f9bcd3255252bf94/Core/IFC/IFC%20S.cs#L1346).

Have I missed any other open formats? [Let me know on twitter!](https://twitter.com/intent/tweet?text=@ddkto%20you%20missed%20a%20format!)