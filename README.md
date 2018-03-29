# WMS
Demo using geomet WMS services
I've not been able to find a good demo of using non-ArcGIS WMS Services in an ArcGIS javascript application. The problem is that there are a lot of moving parts. You can't just create a WMSLayer based upon a GetMap request to a known WMS endpoint and then add it as a layer to a map. Check here https://developers.arcgis.com/javascript/3/jshelp/ags_proxy.html to determine if you need to set up a proxy endpoint on your server. ESRI has created proxy applications for .NET, Java and PHP and they can be found at https://github.com/Esri/resource-proxy
I've included my modified version of their DotNet proxy as a separate folder off of the project root as a convenience - I'll leave the Java and PHP for others interested in those languages. Open the included ReadMe.md inside that folder for instructions on it's deployment and testing. There were a couple modifications made to accomodate the particular geomet WMS Service endpoint, in proxy.config, and to enable Cross Origin Resource Sharing, in Web.config to be found in that folder. Modify them accordingly for your use.
The demo itself is simply a map displaying a WMS layer (surface wind speed in knots) from the federal government environmental weather service at  http://geo.weather.gc.ca/ 
The basemap is the typical ESRI "topo"
