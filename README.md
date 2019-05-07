# ![LOGO](logo.png) Miataru **flow**ground Connector

## Description

A generated **flow**ground connector for the Miataru API (version 1.0.0).

Generated from: https://api.apis.guru/v2/specs/miataru.com/1.0.0/swagger.json<br/>
Generated at: 2019-05-07T17:42:59+03:00

## API Description

The Miataru API is very simple and straight forward. Generally you're posting (HTTP POST) a JSON formatted request to a service method locations and you get back a JSON formatted answer. Please take into consideration that this has the request-for-comment status and that it can change while there's work done on client and server applications. Versioning therefore is done by prepending the version number - /v1/ for version 1 - to the method call.

## Authorization

This API does not require authorization.

## Actions

### To retrieve a specific devices latest known location the /GetLocation method is used. Please note that the MiataruConfig portion is optional. RequestMiataruDeviceID should be the ID of the device the request is sent from (or an identifier like an URL).

*Tags:* `getLocation`

### Retrieves a devices Location in GeoJSON format.

*Tags:* `getLocation`

#### Input Parameters
* `deviceID` - _required_ - the unique device ID of the device the location is requested from

### Location History is stored on the server only if the client told the server to do so using the "EnableLocationHistory" setting in the Location Update requests. For transitions of enabling/disabling that functionality - Everytime a Location Update is received by the server with "EnableLocationHistory=false" the server removes all stored Location History till that point. There is a server-side setting that controls up to how many Location Updates the server is storing in the Location History before it removes the oldest one. To request the Location History of a particular device the client sends the following POST request to the GetLocationHistory service URL. Please note that the MiataruConfig portion is optional. RequestMiataruDeviceID should be the ID of the device the request is sent from (or an identifier like an URL).

*Tags:* `getLocation`

### Visitor History is stored on the server with every request to the location or location history information of a device. There is a server-side setting that controls up to how many Visitors the server is storing in the Visitor History before it removes the oldest one. To request the Visitor History of a particular device the client sends the following POST request to the GetVisitorHistory service URL.

*Tags:* `getVisitorHistory`

### This method is used to update the location of a device. The device does not need to be known already to the Miataru server but it rather creates a unique identifier for itself in the client application. This unique identifier, or device ID is then used to address this particular device.

*Tags:* `updateLocation`

## License

**flow**ground :- Telekom iPaaS / miataru-com-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
