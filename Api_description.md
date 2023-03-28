## The Manitoba Fire-Watch API
### API Description: The Manitoba Fire-Watch API
The Manitoba Fire-Watch Application Programming Interface (API) is a new API that helps the citizens of Manitoba stay informed of fire risks and status across a variety of locations. An API is a set of tools that delivers data based on the requests from a user, and developing the Manitoba Fire-Watch API will increase awareness of fire safety for any citizen of Manitoba looking to spend some time in our great outdoors. 
  
Acting as a two-way road, the API delivers information based on user requests such as location, chance of a fire, the zone the location belongs to, current status of the fire, and the last recorded fire at the given location within Manitoba. This data can also be utilized by National Park Rangers to update their own data and information regarding the fires across our National Parks here in Manitoba, or even emergency services looking to get a quick status update on a blaze.  
  
There are two requests you can make:   
- ```firechance```: The current chance of a fire happening at the given location, and the type of zone that location is in.   
- ```firestatus```: The status of a fire at a given location at the current time. This fire status request also gives the date of the last reported fire at the location.  

### Endpoints and Parameters:
GET
- /firechance/{location}
The endpoint gets the current chance of a fire at the given location. 

- /firestatus/{location}/{currentTime}
The endpoint gets the status of a fire at a given location at the current time.

### Parameter Types:
Location: string
currentTime: int

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

### Sample Request with Sample Response:
Request 1: firechance
Response:
{
  {
    "location": "Birds Hill Park"
  }
  "status": "OK"
}

Request 2: firestatus
Response:
{
  {
    "location": "Riding Mountain National Park"
    "currentTime": 10(in mins)
  }
  "status": "OK"
}


/////////////swagger code//////////
Request 1: firechance
Response:
{
  {
    "id": 1,
    "name": "Birds Hill Wildfire",
    "location": "Birds Hill Park,
    "fire_chance": 0.10,
    "fire_status": "active",
    "is_on_fire": true
  }
}

Request 2: firestatus
Response:
{
  {
    "id": 2,
    "name": "Riding Mountain Wildfire",
    "location": "Riding Mountain National Park",
    "current_time": "10:20:00PM",
    "fire_chance": 0.0,
    "last_fire": "22/07/2022",
    "fire_status": "contained",
    "is_on_fire": false
  }
}












