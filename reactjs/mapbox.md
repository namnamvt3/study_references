MAPBOX

1.what is mapbox?
	- Mapbox is a live location platform that allows developers to create 
		interactive and intuitive map interfaces for a variety of applications
	- Mapbox GL JS is a JavaScript library uses WebGL to render interactive 
		maps from vector tiles and Mapbox styles
	- WebGL is a JavaScript API for rendering interactive 2D and 3D 
		graphics within any compatible web browser without the use of plug-ins
	- vector tile: is a lightweight data format for storing
		> used to create Mapbox vector tilesets
	- Mapbox style is a document that defines the visual appearance of 
	a map: what data to draw, the order to draw it in, and how to style 
	the data when drawing it. A style document is a JSON object with 
	specific root level and nested properties
	
	- react-map-gl which provides React integration for mapbox-gl as 
		well as an easy-to-use component library to build on

2. what is its function?
	- for interactive, customizable vector maps on the web.
	- provides building blocks to add location features like maps, search, 
		and navigation
3. structure

- Installation
	npm install --save react-map-gl
	
	
- Components:

	Mapbox Tokens: 
		To show maps from a service such as Mapbox you will need to 
		register on their website in order to retrieve an access token 
		required by the map component, which will be used to identify 
		you and start serving up map tiles. The service will be free 
		until a certain level of traffic is exceeded
		
		to provide a token to your app:
			Provide a mapboxApiAccessToken prop to the map component
			Set the MapboxAccessToken environment variable (or set 
				REACT_APP_MAPBOX_ACCESS_TOKEN if you are using Create React App)
			Provide it in the URL, e.g ?access_token=TOKEN
			Provide mapboxApiUrl prop to the map component to override the default mapbox API URL
		
	Proxy components (proxy between React and Mapbox API)
		ReactMapboxGL
		Layer & Feature
			property symbol displays a mapbox symbol.
			property line displays a lineString.
			property fill displays a polygon.
			property circle displays a mapbox circle.
			property raster displays a mapbox raster tiles.
			property fill-extrusion displays a layer with extruded buildings.
			property background displays a mapbox background layer.
			property heatmap displays a mapbox heatmap layer.
			Source
		GeoJSONLayer
	DOM components (normal React components)
		ZoomControl
		ScaleControl
		RotationControl
		Marker (Projected component)
		Popup (Projected component)
		Cluster
		
-------------------------------------------
4. example
- to use MapGL > npm install react-map-gl
- to search for a user’s location > npm install react-map-gl-geocoder
- deck-gl, a visualization framework from Uber, to add an overlay marking 
	the area we have searched on our map for greater readability
	> npm install deck.gl