# Email Storage System

The Email Storage API is used to store information extracted from emails and their collections and allows for the pages of attachments to be stored and associated with an email document.

## Get Document List

```
GET https://spamfilter-storageservice-rpa-prod.app.prod.fs.ocp.acmem.corp/api/v1/document?sort=desc&limit=2&status=updated
```

Test the default path request for Email Documents.

### Request

> 
> **Query**
> 
> |Key|Value|Description|
> |---|---|---|
> |sort|desc|The direction (asc/desc) for sorting by the creation. This parameter is **optional** and **acending** is used as the default value.|
> |limit|2|The max number of documents to return. When ommitted the default limit is **10**.|
> |status|updated|The filter to apply to the top level `status` field. If omitted no filtering is done on this field.|
> 

### Examples:

> 
> **Example: Get Document List**
> 
> > 
> > ```
> > GET https://spamfilter-storageservice-rpa-prod.app.prod.fs.ocp.acmem.corp/api/v1/document?sort=desc&limit=2&status=updated
> > ```
> > 
> > **Request**
> > 
> > > 
> > > **Query**
> > > 
> > > |Key|Value|Description|
> > > |---|---|---|
> > > |sort|desc|The direction (asc/desc) for sorting by the creation. This parameter is **optional** and **acending** is used as the default value.|
> > > |limit|2|The max number of documents to return. When ommitted the default limit is **10**.|
> > > |status|updated|The filter to apply to the top level `status` field. If omitted no filtering is done on this field.|
> > > 
> > 
> > **Response**
> > 
> > > 
> > > **Body**
> > > 
> > > ```
> > > [
> > >   {
> > >     "status": "updated", 
> > >     "updated": "2020-11-04T13:16:58.460Z", 
> > >     "created": "2020-11-04T13:16:46.028Z", 
> > >     "text": "The fox has jumped...", 
> > >     "__v": 0, 
> > >     "values": [
> > >       {
> > >         "status": "new", 
> > >         "updated": "2020-11-04T13:16:58.456Z", 
> > >         "created": "2020-11-04T13:16:46.028Z", 
> > >         "text": "Post Email", 
> > >         "values": [], 
> > >         "key": "subject", 
> > >         "_id": "5fa2a9be9cc0a802080e275e", 
> > >         "type": "text"
> > >       }
> > >     ], 
> > >     "key": "post_request.eml", 
> > >     "_id": "5fa2a9be9cc0a802080e275d", 
> > >     "type": "Animal!"
> > >   }, 
> > >   {
> > >     "status": "updated", 
> > >     "updated": "2020-11-04T13:00:23.096Z", 
> > >     "created": "2020-11-04T07:51:25.396Z", 
> > >     "text": "The fox has jumped...", 
> > >     "__v": 0, 
> > >     "values": [
> > >       {
> > >         "status": "new", 
> > >         "updated": "2020-11-04T13:00:23.080Z", 
> > >         "created": "2020-11-04T07:51:25.395Z", 
> > >         "text": "Post Email", 
> > >         "values": [], 
> > >         "key": "subject", 
> > >         "_id": "5fa25d7de0eb6a3dc2f020bf", 
> > >         "type": "text"
> > >       }
> > >     ], 
> > >     "key": "post_request.eml", 
> > >     "_id": "5fa25d7de0eb6a3dc2f020be", 
> > >     "type": "Animal!"
> > >   }
> > > ]
> > > ```
> > > 
> > 
> 

## Get Single Email Document

```
GET http://localhost:3000/api/v1/document
```

Find a single email document by id.

## Delete Request

```
DELETE http://localhost:3000/api/v1/document/5f9983b699274c2f309fd4cd
```

Test deleting a email document.

## Post Request

```
POST http://localhost:3000/api/v1/document
```

Check to see if the post route is working.

### Request

> 
> **Body**
> 
> ```
> { 
>     "key" : "post_request.eml", 
>     "type" : "Email", 
>     "text" : "Post request email body",
>     "values" : [
>         {
>             "key" : "subject", 
>             "type" : "text", 
>             "text" : "Post Email"
>         }
>     ]
> }
> ```
> 

## Create Netsted Email Document

```
POST http://localhost:3000/api/v1/document
```

Test the schema validation of nested items.

### Request

> 
> **Body**
> 
> ```
> { 
>     "key" : "post_request.eml", 
>     "type" : "Email", 
>     "text" : "Post request email body",
>     "values" : [
>         {
>             "key" : "subject", 
>             "type" : "text", 
>             "text" : "Post Email"
>         }
>     ]
> }
> ```
> 

## Post Request  - Error Testing

```
POST http://localhost:3000/api/v1/document
```

Check to see if the post route is working.

### Request

> 
> **Body**
> 
> ```
> { 
>     "type" : "Email", 
>     "text" : "Post request email body",
>     "values" : [
>         {
>             "key" : "subject", 
>             "type" : "text", 
>             "text" : "Post Email"
>         }
>     ]
> }
> ```
> 

## Put Request

```
PUT http://localhost:3000/api/v1/document/5fa14115ea4bab39cbd17889
```

Check to see if the put route is working and accepting an id.

### Request

> 
> **Body**
> 
> ```
> {
>     "text": "The fox has jumped...",
>     "type": "Animal!"
> }
> ```
> 

## Get Request

```
GET https://spamfilter-storageservice-rpa-prod.app.prod.fs.ocp.acmem.corp/api/v1/image/5fa3ca9bb4fa9e0604f5002f
```

Get an email image by ID.

## Upload Image

```
POST http://localhost:3000/api/v1/image/upload
```

Upload an image

### Request

> 
> **Body**
> 
> |Key|Value|Type|Description|
> |---|---|---|---|
> |file||file||
> |metadata|{"srNumber": "EC-1Z23-3QDBEJ"}|text||
> 

## Delete Image

```
DELETE http://localhost:3000/api/v1/image/5fa3c929d7cbdd05ab940ec2
```



Generated with [Postdown][PyPI].

[PyPI]:    https://pypi.python.org/pypi/Postdown
