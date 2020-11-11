# Email Storage: Images

 These API methods allows for the images of attachment pages to be stored and associated with an email document.

## Delete Image

```
DELETE http://localhost:3000/api/v1/image/5fa3c929d7cbdd05ab940ec2
```



## Stream Image

```
GET https://spamfilter-storageservice-rpa-prod.app.prod.fs.ocp.acme.corp/api/v1/image/5fa3ca9bb4fa9e0604f5002f
```

Stream the image with the ID as specified in the URL. Links such as these can be used in `img` tags for display on an HTML page.

### Examples:

> 
> **Example: Get Request**
> 
> > 
> > ```
> > GET https://spamfilter-storageservice-rpa-prod.app.prod.fs.ocp.acme.corp/api/v1/image/5fa3ca9bb4fa9e0604f5002f
> > ```
> > 
> 

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

Generated with [Postdown][PyPI].

[PyPI]:    https://pypi.python.org/pypi/Postdown
