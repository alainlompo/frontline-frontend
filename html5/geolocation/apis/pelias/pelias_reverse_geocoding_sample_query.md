<h3>Sample illustration about running a reverse geocoding request from mapzen search</h3>

The query:
**********
-s "search.mapzen.com/v1/reverse?size=1&point.lat=40.74358294846026&point.lon=-73.99047374725342&api_key={YOUR_API_KEY}" | json

The result:
***********
<pre>
{
	"geocoding":
	{
		"version":"0.1",
		"attribution":"https://search.mapzen.com/v1/attribution",
		"query":{"size":1,"private":false,"point.lat":40.74358294846026,"point.lon":-73.99047374725342,"boundary.circle.radius":500,"boundary.circle.lat":40.74358294846026,"boundary.circle.lon":-73.99047374725342,"querySize":1},"engine":{"name":"Pelias","author":"Mapzen","version":"1.0"},
		"timestamp":1461292137218},
		"type":"FeatureCollection",
		"features":[{"type":"Feature","geometry":{"type":"Point","coordinates":[-73.99051,40.74361]},
		"properties":{"id":"9851011","gid":"geonames:venue:9851011","layer":"venue","source":"geonames","name":"Arlington","confidence":0.9,"distance":0.004,"country":"United States","country_gid":"whosonfirst:country:85633793","country_a":"USA","region":"New York","region_gid":"whosonfirst:region:85688543","region_a":"NY","county":"New York County","county_gid":"whosonfirst:county:102081863","locality":"New York","locality_gid":"whosonfirst:locality:85977539","borough":"Manhattan","borough_gid":"whosonfirst:borough:421205771","neighbourhood":"Flatiron District","neighbourhood_gid":"whosonfirst:neighbourhood:85869245","label":"Arlington, Manhattan, New York, NY, USA"}}],
		"bbox":[-73.99051,40.74361,-73.99051,40.74361]
}
</pre>