#	Uniform API Viewer
---
 
## Motivation
It bugs me up, that many many frameworks/librarys out there still come up with ugly 
structured and designed API documentations and/or manuals. However, once checked how 
to use the docs, I always find the information I am looking for. But at the end, those repetetive 
procedures become the less quick and intuitive the scruffier those informations are structured.  

To avoid such "workflow blockers" in the future, I decided to develop "something" that gives me 
API docs and other references straight to my fingertips. Nothing should be more than three clicks 
away and everything should be formated in a typographically pleasuring way so that specific
things can be found straightaway.

Further, all API documentations should be joined into a single data file, that will be
part of the Viewer Application. So they will always be available -- regardless whether a connection
to the internet will be available or not.

This project's intention primarily targets dynamic (scripting) languags; especially JavaScript
with its jungle of libraries, frameworks and their respective masses of 3rd-party plugins/additions. 
Although the popular projects like jQuery, YUI and since this week even MooTools already have official
platforms for publishing 3rd-party plugins/additions, where links to author websites and API 
documentations can be found, though, they're kind of cluttered. That's why one of the main purposes
of this project is it to include even API docs of 3rd-party plugins for miscellaneous frameworks/libraries,
giving developers all those stuff right under their belt. Everytime and everywhere.  

## Overview
Essentially, the UAV project is divided into two main parts:

	1. A XML-dialect used to uniformly describe APIs, called _Uniform API Document (UAPID)_
	2. The Viewer-Application for UAPID files
	
### The UAPID data format
The _UAPID_- dataformat is a custom XML-dialect modelled to meet the requirements of 
describing Application Programming Interfaces of miscellaneous dynamic (scripting) languages 
with all their specifics. To assert that UAPIDs will always be consistent and to allow 3rd-party
developers to contribute their own UAPIDs, I modelled a full-fledged XML Schema that can
be used for reference purposes when writing XSL Transformations or converters.

In the near future, I intend to release XSLTs which use publicly available API docs as source
and transform them to suitable UAPIDs. Meaning that every user can update his UAPIDs on his own.
Another mark in the roadmap will be the creation of an online UAPID repository, where users can
"compile" custom UAPID-libraries. 

Further details can be found in the repository folder called _"UAPID Specification"_.

### The Viewer-Application
Just serving as simple and robust Viewer Application with emphases on **typographic pleasure**, 
**usability** and a few decent but handy extra-features. No blown up memory hug or exposee for 
what's possible with JavaScript animations. Cause it bases on the latest version of the Adobe AIR-platform, 
every developer, whether working on a Windows, Mac OS or *nix machine can leverage the conveniences
of UAP.

### FAQ
#### Why are you using XML as driving force instead of JSON?
Well, despite XML isn't as compact as JSON, it is literally still the most versatile data basis
for my purposes. With the XML Schema for _Uniform API Documents_ I defined a reference structure 
that serves as basis for any internal XSLT-heavy convertions, while remaining flexible for any further
developments (maybe using [YUI Doc](http://developer.yahoo.com/yui/yuidoc/ "YUI Doc project page") for generating coherent API references). Althoug the guys around
Dojo have created a similar approach with [JSON Schema](http://json-schema.org/), its implementation
isn't as mature and as widely adopted as those of XML Schema yet. Beside that, if anybody wants to
have UAPIDs written in the JSONotation, converting them from XML to JSON should be a breeze.

#### Why the heck do you want to bring those API docu stuff onto the client-side? Going onto the the according project website and having a quick look isn't that time consuming.
As already stated above, at its sum, it is. Beside that, I have always opened a bunch of tabs with
iGoogle, Google Reader and other interesting stuff ... and I dunno why, but their always attracting 
my attention in a magical way it can't resist. ;-) So having everything at Space 3 (yeah, Hackintosh)
calms and keeps my focus where it remains to -- the code.


## Technical Details
### _Uniform API Document_ Format
	*	XML
	*	XML Schema
	*	XSLT 2.0 (using Saxon EE)
Tools with a GUI for editing and authoring UAPIDs will follow. Probably something based on XHTML, CSS & JavaScript.

### Viewer Application
	*	Adobe AIR 2.0b (using the JS-bridge)
	*	HTML & CSS
	*	JavaScript

## Roadmap
	*	Testing & finishing the UAPID schema
	*	Building a workflow for authoring UAPIDocuments
	*	Developing a prototype of the Viewer Application
	*	Testing & finishing the Viewer Application