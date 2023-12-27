# ArcGis
Location tracking application POC

********************* Backend *********************

This is the backend end portion of the ArcGis POC project - communicates with the angular front end which is located in ArcGISLocationMappingFE Repo 
Download project and import in eclipse before anything. Set up workplace as well
Will need Spring, Java, and maven installed.

Run maven clean install before starting

Update Pom.xml with any dependencies you may need, then right click and update project in "Maven" and add <relativePath></relativePath> under <parent>

If you need to use different db, src/main/resources/application.properties has DB connection info.

If you want to use your own ArcGis API Key, generate one and update line 48 in PoiService.java

Table name: Locations, to update this -> update line 10 on Location.java

Make sure WebConfig.java is within the project files structure, otherwise it will not be able to communicate with the frontend. 

LocationService.java handles most DB transactions. Update this class however you like, save function is in PoiService.java

If you add more fields in Location model, make sure to add getters and setters for those fields otherwise they will not populate in DB

********************* Frontend *********************

This is the front end portion of the ArcGis POC project - communicates with the Java backend and DB which are both located in ArcGISLocationMappingBE Repo 

Run npm i before starting 

run npm start to run application
