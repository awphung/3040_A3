## API Description Document
### API Description: The Manitoba Fire-Watch API
The Manitoba Fire-Watch API is a new API that helps the citizens of Manitoba stay informed of fire risks and status across a variety of locations. The API delivers data such as the location, chance of a fire, the zone the location belongs to, current status of the fire, and the last recorded fire at the given location within Manitoba. This data can also be utilized by National Park Rangers to update their own data and information regarding the fires across our National Parks here in Manitoba.  
  


### Endpoints and Parameters:
- /firechance/{location}

- /firestatus/{location}/{currentTime}

### API Resources:
{  
&emsp; "location": "Birds Hill Park",  
&emsp; "firechance": "0.10",  
&emsp; "zone": "green"  
}  
  
{  
&emsp; "location": "Riding Mountain National Park",  
&emsp; "status": "no fire",  
&emsp; "lastfire": "22-07-2022"  
}