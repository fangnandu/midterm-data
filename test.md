
# Open Source Tools For GIS 

## -  Week 1 and 2
#### Code Academy
* Complete Units in the Course Academy [Javascript coursework](https://www.codecademy.com/learn/javascript)
  - Introduction to JavaScript
  - Variables and data types
  - Control Flow
  - Functions
  - Scope
  - Arrays
  - Loops
  - Iterators
  - Objects
  

## -  Week 3
#### 1.Section 1: Using functions (liberally!)
* Function anatomy
  - Naming/defining functions vs calling functions
  - Providing arguments
  - The function body
  - The `return` statement
* Thinking functionally
  - Programs are data and its transformations
  - Functions are just transformations on data
  - Functions as values
#### 2.Live coding: refactoring code into functions
* Step through the code and discuss
* Imagine alternative code flows
* Organize the code
* Make code DRYer ('don't repeat yourself')
    - Redundant code is a headache to maintain
    
#### 3.underscore.js

## -  Week 4


#### Section 1: Underscore Review
- More Underscore utilities
- Underscore scavenger hunt 2

#### Section 2: jQuery & Async Behavior
- jQuery
  - Library motivation
  - Getting data from elsewhere
  - [ajax](http://api.jquery.com/category/ajax/)
- Programming in time
  - Working with (future) data
  - Managing state

#### Section 3: Complete HTML/CSS
  - HTML Basics
  - Build your own webpage
  - HTML Basics 2
  - CSS: An Overview
  
## -  Week 5  
  
#### More developer tools
  - Viewing/playing with HTML and CSS in `elements`
  - 'Breakpoint debugging' in `sources`
  - Viewing data transfer in `network`
- Homework/lab discussion
  - Thinking through asynchronous behavior and scope
  - Walk through async code example
  - Walk through CSS/HTML example
- Thinking of functions in terms of what they do vs what they are
  - `return` statements
  - `_.map` vs `_.each`

##### jQuery Continued
- Element selection
  - A central feature of jQuery
  - CSS selectors
- jQuery events
  - 'Binding' events to elements
  - Asynchronous behavior (just like ajax)
  
  
 ## -  Week 6
 
#### CSS Review

- Answering CSS questions
- Box Model
- Position: static, relative, absolute

#### Lecture & Labs
- Box Model
- Position: static, relative, absolute
- Absolute position lab
- Design overview
- Figma lab / assignment

## week 7
### Advanced Cartography

##### Section 1: GeoJson & Leaflet
- Plotting geojson
  - What is JSON? (Remember `JSON.parse`?)
  - Filtering for individual geojson elements
  - Styling individual geojson elements
- Making a legend in HTML with Leaflet and jQuery

##### Section 2: Getting Geospatial Data
- Where to find it
- Formatting and converting it
- Using github as a backend (storage)
- Creating it with geojson.io


## week9
### Introduction
- turf.js (example only)
  - Spatial join demo
  - Measurement extraction
  - Aggregation and analysis
  - Other stuff (classification, interpolation, utility methods)
- Leaflet draw (a plugin for the leaflet library)
  - Generate polygons, points, and lines from user interaction
- Mapbox APIs
  - Free(ish) alternative to writing backend code
  - Powerful (though limited for free users)
  - Geocoding
  - Routing


### Interaction and analysis

##### Section 1: Leaflet Draw
- Plugin introduction

##### Section 2: Mapbox Utilities
- In-class exploration of experimentation with an API

## week 10
### Frontend Frameworks
  - Components
    - Button groups
    - Input groups
    - Glyphicons
  - Javascript
    - Tooltips
    - Modal
    - Dropdown
  - CSS
    - Grid
    - Tables
    - Forms
- Carto

## week 11


### SQL Related
- SQL with CartoDB
  - Manually writing SQL for analysis
  - Always:clap:use:clap:the:clap:SQL:clap:console:clap:
  - SQL [types](https://www.postgresql.org/docs/9.5/static/datatype.html), special Carto columns, and PostGIS [types](https://postgis.net/docs/reference.html#PostGIS_Types)
  - [Creating new
    tables](https://github.com/CartoDB/cartodb/wiki/creating-tables-though-the-SQL-API)
  - Results as GeoJSON
- SQL Resources
- Examples
  - Torque for time series
  - SQL for persisting data changes, interaction, and GeoJSON

### PostgreSQL & PostGIS Resources
#### GIS Extension Related
> Good

- [PostGIS special function
index](https://postgis.net/docs/PostGIS_Special_Functions_Index.html)
- [PostGIS reference docs](http://postgis.net/docs/reference.html)
- [Stack exchange's GIS-specific subdomain](gis.stackexchange.com/)

#### Examples

[CartoDB Torque](./examples/torque/)
Torque.js is an open source library for creating dynamic visualizations for
your time series data on top of Leaflet (and with the help of CartoDB).
If you're dealing with time and space, Torque can build compelling
visualizations ranging over both dimensions.


[CartoDB SQL API](.examples/writing-data/)
> Keeping API keys in client applications is NOT a safe practice.
> Do NOT use the techniques from this lab in the wild.

## Week 12

- GeoJSON and SQL through CartoDB
  - REMINDER: Always:clap:use:clap:the:clap:SQL:clap:console:clap:
  - You can use a REST client like
    [Postman](https://www.getpostman.com/) or [Advanced REST
Client](https://chrome.google.com/webstore/detail/advanced-rest-client/hgmloofddffdnphfgcellkdfbfbjeloo?hl=en-US)

- Carto Input/Output
  - [Result formats](https://carto.com/docs/carto-engine/sql-api/making-calls#response-formats)
  - [Carto backed maps](examples/carto)

- [SQL Performance](https://carto.com/docs/carto-engine/sql-api/query-optimizations)
  - Ask for only the columns you need
  - [Geometry simplification](http://www.postgis.org/docs/ST_Simplify.html)
  - [Indices](http://revenant.ca/www/postgis/workshop/indexing.html)
  - [Save work in new tables](https://www.postgresql.org/docs/8.2/static/sql-createtableas.html)
  - [Force CARTO to recognize new tables](https://carto.com/docs/carto-engine/sql-api/creating-tables/)
  - Use the `cartodb_id` in queries (this column is indexed by default). Example:
```SQL
SELECT
  *
FROM
  <TABLE>
WHERE
  cartodb_id = <some_id>
```

- Rasters
  - Tiling for TMS
  - PostGIS analysis (this is painful - I've always avoided it and you should too)
  - Alternatives


- Extras:
  - [Fast spatial joins on the frontend with rtrees](https://beta.observablehq.com/@jfrankl/spatial-search-with-flatbush-and-leaflet-draw) (demo by Jeff Frankl) Note that these joins work with bounding boxes rather than complex shapes
  - [Working with topojson](https://beta.observablehq.com/@jfrankl/topojson) (demo by Jeff Frankl)
  - [Project work by the creator of Leaflet](https://github.com/mourner/projects) Quoting Jeff: "*rbush* can handle points and rectangles and can be updated, *flatbush* is faster than rbush but is static (can’t be updated with new geoms), *kdbush* is the fastest but is only for points"

