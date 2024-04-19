# Easier Apis - Endpoints
## Usage
The endpoint function is used to set an api endpoint, that can be used in a client or fetched by a browser.

## Syntax (* required)
```javascript
api.endpoint({ parameters }*, callback*);
```
The callback is defined using:
```jasvascript
(req*, res*, params*, file, filename) => {}
```

## All Parameters (* required)
- url* (Simple, its the endpoint.)
- acceptFile (Which accepts file from the request, and places it in the fileLocation, if true)
- fileLocation (default: 'uploads/')
- fileName (default: date + time, to prevent conflicts)
- fileType (default: 'any')
- origin ( This restricts to only one origin )
- originMessage (default: 'Permission Denied', this is the data sent back to the client when the origin does not match. )
```javascript
{ url: "/endpoint/", acceptFile: false, fileLocation:'images/jpg', fileName: "testFile.jpg". fileType: "image/jpeg", origin: "localhost:3000", originMessage: "No access."}
```

## Static Endpoints
Static endpoints can be defined by calling staticendpoint() and perform the same function as an endpoint, but returns a static value.
Here are all the parameters:
- url* (Simple, its the endpoint.)
- origin ( This restricts to only one origin )
- originMessage (default: 'Permission Denied', this is the data sent back to the client when the origin does not match. )
```javascript
api.staticendpoint({ url: '/endpoint/'*, origin: 'loaclhost:3000', originMessage: 'No access.'}, 'hello!')
```
