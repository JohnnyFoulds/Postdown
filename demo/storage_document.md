# Email Storage: Document

----------------

The Email Storage Document API is used to store information extracted from emails and their attachments.

----------------

## Get Document List

```
GET https://spamfilter-storageservice-rpa-prod.app.prod.fs.ocp.acme.corp/api/v1/document?sort=desc&limit=2&status=updated
```

Test the default path request for Email Documents.

----------------

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

----------------

## Get Single Email Document

```
GET http://localhost:3000/api/v1/document
```

Find a single email document by id.

----------------

### Request

> 
> **Query**
> 
> |Key|Value|Description|
> |---|---|---|
> ||||
> 

### Examples:

> 

----------------

## Delete Request

```
DELETE http://localhost:3000/api/v1/document/5f9983b699274c2f309fd4cd
```

Test deleting a email document.

----------------

### Request

> 
> **Query**
> 
> |Key|Value|Description|
> |---|---|---|
> ||||
> 

### Examples:

> 

----------------

## Post Request

```
POST http://localhost:3000/api/v1/document
```

Check to see if the post route is working.

----------------

### Request

> 
> **Query**
> 
> |Key|Value|Description|
> |---|---|---|
> ||||
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

### Examples:

> 

----------------

## Create Netsted Email Document

```
POST http://localhost:3000/api/v1/document
```

Test the schema validation of nested items.

----------------

### Request

> 
> **Query**
> 
> |Key|Value|Description|
> |---|---|---|
> ||||
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

### Examples:

> 

----------------

## Post Request  - Error Testing

```
POST http://localhost:3000/api/v1/document
```

Check to see if the post route is working.

----------------

### Request

> 
> **Query**
> 
> |Key|Value|Description|
> |---|---|---|
> ||||
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

### Examples:

> 

----------------

## Put Request

```
PUT http://localhost:3000/api/v1/document/5fa14115ea4bab39cbd17889
```

Check to see if the put route is working and accepting an id.

----------------

### Request

> 
> **Query**
> 
> |Key|Value|Description|
> |---|---|---|
> ||||
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

### Examples:

> 

----------------

----------------

Built with [Postdown][PyPI].

Author: [Titor](https://github.com/TitorX)

[PyPI]:    https://pypi.python.org/pypi/Postdown