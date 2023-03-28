## API Description Document
### API Description: The Manitoba Fire-Watch API
T  
The API includes data such as the location, size, intensity, and direction of the fire within Manitoba. This data can be used by emergency services, researchers, and the general public to monitor and respond to wildfires in the area. People can use this API to report the size and location of wildfires as well.

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