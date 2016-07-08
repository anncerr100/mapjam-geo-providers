# mapjam-geo-providers

Supports Esri/Arcgis, Google, Mapzen, Nokia/HERE Geocode and Reverse Geocode

## Installation

  `npm install mapjam-geo-providers`

## Usage

	var geo = require('mapjam-geo-providers');

	var latlng = ['37.750629', '-122.439880'];


	var mapzen_key = {"api_key":"YOUR_KEY"};
	var HERE_key = {"app_id":"YOUR_APP_ID", "app_code":"YOUR_APP_CODE"};


	//reverse geocode
	geo.geocode('mapzen',latlng, mapzen_key, function(err,resp){
		if(err) {
		  console.log(err);
		} else {
		  console.log('Reverse GEO RESULT=====>', resp);
		}
	});

	//geocode
	geo.geocode('mapzen','814 mission st san francisco', mapzen_key, function(err,resp){
		if(err) {
		  console.log(err);
		} else {
		  console.log('Geo RESULT=====>', resp);
		}
	});