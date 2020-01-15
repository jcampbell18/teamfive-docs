# To configure new location: start with a new location with zero objects
This example uses location ID 7 as an example

## Step 0: Create Location and note the primary and secondary lat/long and image x/y (image x/y via point-and-click)
/location/new

primary
lat: 47.489562	
long: -117.585686

secondary
lat: 47.490153
long: -117.585083

## Step 1: Create primary object:
/object/new

{
	short_name: "primary"
	description: ""
	active: "1"
	location_id: "7"
	long_name: ""
	x_coordinate: 0
	y_coordinate: 0
	image_x: "84"
	image_y: "118"
	object_type_id: 4
	latitude: "47.489562"
	longitude: "-117.585686"
}

## Step 2: Create secondary object: 
/object/new

{
	short_name: "secondary"
	description: ""
	active: "1"
	location_id: "7"
	long_name: ""
	x_coordinate: 0
	y_coordinate: 0
	image_x: "483"
	image_y: "697"
	object_type_id: 5
	latitude: "47.490153"
	longitude: "-117.585083"
}

## Step 3: Set Scale:
/location/set-scale/7

When SELECT * FROM objects WHERE location_id = e.g. 7 you should see:

object_id,location_id,short_name,long_name,description,object_type_id,x_coordinate,y_coordinate,image_x,image_y,latitude,longitude,active
264,7,primary,,,4,0,0,84,118,47.489562,-117.585686,1
265,7,secondary,,,5,218,146,483,697,47.490153,-117.585083,1


