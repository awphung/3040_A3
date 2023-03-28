## API Description Document
### API Description: The Manitoba Fire-Watch API
The Manitoba Fire-Watch API is a new API that helps the citizens of Manitoba stay informed of fire risks and status across a variety of forested locations. The API delivers data such as the location, chance of a fire, the zone the location belongs to, current status of the fire, and the last recorded fire at the given location within Manitoba. This data can also be utilized by National Park Rangers to update their own data and information regarding the fires across our National Parks here in Manitoba, or even emergency services looking to get a quick status update.  
  
There are two requests you can make:   
- ```firechance```: The current chance of a fire happening at the given location, and the type of zone that location is in.   
- ```firestatus```: The status of a fire at a given location at the current time. This fire status request also gives the date of the last reported fire at the location.  

### Endpoints and Parameters:
- /firechance/{location}

- /firestatus/{location}/{currentTime}

### API Resources:
firechance:  
{  
&emsp; "location": "Birds Hill Park",  
&emsp; "firechance": "0.10",  
&emsp; "zone": "green"  
}  
  
firestatus  
{  
&emsp; "location": "Riding Mountain National Park",  
&emsp; "status": "no fire",  
&emsp; "lastfire": "22-07-2022"  
}