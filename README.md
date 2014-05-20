GraphHopper Web API
=======

With [GraphHopper Web API](http://graphhopper.com/#enterprise) it is possible to get the 
fastest path between two or more locations. Additionally to the Open Source API it is 
possible to use addresses as location, not only coordinates. This process is called *Geocoding*.


## How to Start

 1. To use the API you need credentials, please [contact us](http://graphhopper.com/#enterprise).
 2. Read the documentation for **Routing** and **Geocoding**, see below.

Also you can see routing and geocoding in action at [GraphHopper Maps](http://graphhopper.com/maps).

## Issues

If you have problems please report them [here](https://github.com/graphhopper/web-api/issues). 
If you are not a customer or found a bug directly in the Open Source code please report it 
[here](https://github.com/graphhopper/graphhopper/issues) instead.

## Routing API

![Routing Example](./img/routing-example.png)

The JSON format of the hosted Web API is 100% identical to the [Routing API](https://github.com/graphhopper/graphhopper/blob/master/docs/web/api-doc.md) response format.

The endpoint is `http://graphhopper.com/api/[version]/route`

An example URL looks like:

`http://graphhopper.com/api/1/route?point=51.131108%2C12.414551&point=48.224673%2C3.867187&vehicle=car&locale=de&key=[your-key]`

## Geocoding API

![Geocoding Example](./img/geocoding-example.png)

The Geocoding API is documented [here](./docs-geocode.md).

The endpoint is `http://graphhopper.com/api/[version]/geocode`

An example URL looks like:

`http://graphhopper.com/api/1/geocode?q=berlin&locale=de&key=[your-key]`

Append `&debug=true` for a formatted output.

<!--
## Isochrone API

![Isochrone Example](./img/isochrone-example.png)

The Isochrone API is documented [here](./docs-isochrone.md).

The endpoint is `http://graphhopper.com/api/[version]/isochrone`

An example URL looks like:

`http://graphhopper.com/api/1/isochrone?q=52.511624,13.438339&time_limit=1200&vehicle=car&key=[your-key]`

Append `&debug=true` for a formatted output.
-->

## Attribution

The standard package requires a prominent attribution of GraphHopper. This means you have to include a link to graphhopper.com where you utilize the GraphHopper Web API. It is important to note that the user has to see this only one time e.g. per application start or at the first website access. The user must have the possibility to click on the link e.g. including it only in a splash screen isn't appropriate where as including this in or below a search input is appropriate. For an example you can look at [GraphHopper Maps](http://graphhopper.com/maps/)

An html snippet for this is:

```html
powered by <a href="http://graphhopper.com">GraphHopper</a>
```

If you need a custom or white-label solution please contact us.

Regardless of the package and additionally to our attribution you need to include attribution to [OpenStreetMap](http://www.openstreetmap.org/copyright/).

## HTTP Error codes

HTTP error code | Reason
:---------------|:------------
500             | Internal server error. It is strongely recommended to send us the message and the link to it, as it is very likely a bug in our system.
501             | Only a special list of vehicles is supported
400             | Something was wrong in your request
401             | Authentication necessary
403             | Not paid or API limit reached
