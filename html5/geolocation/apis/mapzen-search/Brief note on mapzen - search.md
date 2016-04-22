<h3>Geocoding with mapzen</h3>
<br/>

mapzen is a cool geographic service powered by open source tools and open data. It access is based on the common pattern of using an API Key, which can be obtained
on <a href='https://mapzen.com/developers'>the developers web site</a> after you authenticate using your github account. In our illustration (The starter.html file in the same folder) we used the Leaflet library to set a View on Oakland California, with enough zooming so as to be able to seet the streets names. Here is a snapshot of it:<br/>

<b>Fig. 1: Oakland, California from mapzen-search</b>
<img src='https://github.com/alainlompo/frontline-frontend/blob/master/html5/geolocation/apis/mapzen-search/Oakland_california.png' />

Mapzen search uses <b>geocoding</b> via <i>natural language inputs</i> to find particular places (using names, landmarks, businesses) and translate it into geographical coordinates
Mapzen has also some <b>reverse geocoding features</b> that transform some geographical coordinate (longitude and latitude) into a list of places. Our second illustration is about performing search on an already displayed map using the search icon which display an input box. Of course we can query the entire database or target something related to the displayed geographical area<br/>

<b>Fig. 2: Franklin square, New York from mapzen-search search box</b>
<img src='https://github.com/alainlompo/frontline-frontend/blob/master/html5/geolocation/apis/mapzen-search/Frankling_square_new_york_via_search_box.png' />

