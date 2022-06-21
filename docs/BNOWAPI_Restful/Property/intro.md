---
sidebar_position: 2
slug : /bnowapi_restful_interface/property
title: Property Information
---

#  Property Information

Enpoint
All the call must be made to the the following end point using https procotol.
### Get property information
Retuns the information of a property
```
Authorization: Basic Zm9vOmJhcg==
```
Response Formats json/xml
Response format is defined by the request Accept header
### Header

```
Content-Type: application/x-www-form-urlencoded
```

###  GET 

```
/Property/:id
```


### Parameter

| Field 	|   Type   	|                                      Description                                      	|                                      Description                                      	|   	|
|:-----:	|:--------:	|:-------------------------------------------------------------------------------------:	:-------------------------------------------------------------------------------------:	|---	
| id    	|  String  	|   The Property-ID. (NOTE: CALL /property WITHOUT ANY PARAMETER TO GET ALL PROPERTIES) 	|   The Property-ID. (NOTE: CALL /property WITHOUT ANY PARAMETER TO GET ALL PROPERTIES) 
Get property information

Retuns the information of a property
#  Success Response (200)


|  **Field**  	    |    **Type**    	    |               **Description**              	|
|:-----------:  	|:--------------:	    |:------------------------------------------:	|
| hotel_id    	    |  Number        	    |    unique hotel identifier                 	|
| name        	    |  string        	    |   The name of the hotel                    	|
| street      	    |  string        	    |   The address of the hotel.                	|
| city        	    |  string        	    |   City of the hotel.                       	|
| country       	|  string           	|   Country of the hotel                     	|
| latitude    	    |  Number            	|   Latitude of the hotel                    	|
| longitude     	|  Number          	|   Longitude of the hotel                   	|
| url           	|  string           	|   The bookonline now URL of the hotel      	|
| phone        	|  String           	|   Phone number of the hotel.               	|
| email           	|  String           	|   email address of the hotel.              	|
| fax          	|  String        	    |   Fax number of the hotel                  	|
| postcode      	|  String           	|   Postcode number of the hotel             	|
| photos      	    |   Photo array     	|   An array of photo objects for the hotel  	|
| description   	|  string        	    |   Description of Hotel.                    	|
| amenities     	|  string        	    |   Amenities of Hotel.                      	|

