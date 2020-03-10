#  API Documentation Template 

## Title

<Describe API call. Verbs that match request type and one or many, etc. *GetUsers*>

## URL

<URL Structure (path without base)>

## Method:

<The request type>

DELETE | GET | POST | PUT


## URL Parameters

<URL parameters if they exist and whenther optional.>

/users/:id


### Required:

id [int]


### Optional:

name# [string]

### POST Params

<If POSTing describe payload here.>

### Success Response:

<What should the status code be on success, and return type/data.>

Code: 200
Content: { id : 12 }


### Error Response:

<List ALL possible Error responses>

Code: 401 UNAUTHORIZED
Content: { error : "Log in" }

Code: 444 UNPROCESSABLE
Content: { error : "User exists" }



### Example Call:

### Get list of Things

#### Request

`GET /thing/`

    curl -i -H 'Accept: application/json' http://localhost:7000/thing/

#### Response

    HTTP/1.1 200 OK
    Date: Fri, 24 Apr 2009 07:13:21 GMT
    Status: 200 OK
    Connection: close
    Content-Type: application/json
    Content-Length: 2

    []
  

## Get a specific Thing

### Request

`GET /thing/id`

    curl -i -H 'Accept: application/json' http://localhost:7000/thing/1

### Response

    HTTP/1.1 200 OK
    
    Date: Fri, 24 Apr 2009 07:18:42 GMT
    Status: 200 OK
    Connection: close
    Content-Type: application/json
    Content-Length: 36

    {"id":1,"name":"Foo","status":"new"}

    
Notes:

