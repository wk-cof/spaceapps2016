##Add a command to the queue:
```HTTP
POST /alexa/request HTTP/1.1
Host: SuitePort.mybluemix.net
Content-Type: application/javascript
Cache-Control: no-cache
Postman-Token: dc919ab9-ed93-dfde-2149-612b7b59d6cb

{
    "location": "mars",
    "intent": "takeMe"
}
```

**Sample response**
```javascript
{
  "ok": true,
  "id": "e862d01a031e7fa69d86cd62cb6b04b3",
  "rev": "1-ebad2a2de44302803dabc0288fdd8458"
}
```

##Read all commands from the queue:
```HTTP
GET /requests HTTP/1.1
Host: SuitePort.mybluemix.net
Cache-Control: no-cache
Postman-Token: 227d7717-95cc-993e-b0ed-f80c8490a05f

```

**Sample response**
```javascript
[
  {
    "_id": "e862d01a031e7fa69d86cd62cb6b04b3",
    "_rev": "1-ebad2a2de44302803dabc0288fdd8458",
    "timestamp": 1461471126501
  },
  {
    "_id": "974aece55c4979ee4a5d84454f64aa12",
    "_rev": "1-3dc339fcec9971a23eb3d5c84efbfd0a",
    "timestamp": 1461471254924
  }
]
```

##Read 1 command from the queue:
```HTTP
GET /requests/974aece55c4979ee4a5d84454f64aa12 HTTP/1.1
Host: SuitePort.mybluemix.net
Cache-Control: no-cache
Postman-Token: 2c9cfaf8-7592-6e1c-82d4-274b62af6d84
```

**Sample response**
```javascript
{
  "_id": "974aece55c4979ee4a5d84454f64aa12",
  "_rev": "1-3dc339fcec9971a23eb3d5c84efbfd0a",
  "timestamp": 1461471254924
}
```

##Delete a command:
```HTTP
DELETE /requests/974aece55c4979ee4a5d84454f64aa12 HTTP/1.1
Host: SuitePort.mybluemix.net
Cache-Control: no-cache
Postman-Token: 4e200a6f-422e-0310-4e49-e318ff221ec3
Content-Type: multipart/form-data; boundary=----WebKitFormBoundary7MA4YWxkTrZu0gW
```

**Sample response**
```javascript
{
  "ok": true,
  "id": "974aece55c4979ee4a5d84454f64aa12",
  "rev": "2-4e28de870054db3ee80271e44d5bed1b"
}
```
