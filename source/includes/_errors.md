# Errors

Every error returned by the CrowdTangle API will assume a standard format. The API will additionally return a proper http status as well. If a `200` is returned, there was no error. 

<aside class="notice">
If a <code>200</code> is returned, there was no error.
</aside>

## Error Response
>Error Response

```json

{
  "status": 401,
  "code": 30,
  "message": "Please supply an API token"
}
```

Property | Type | Description
---------|------|-------------
code | int | The [CrowdTangle error code](https://github.com/CrowdTangle/API/wiki/Errors#errorcodes), if available.
message | string | A human-readable message describing the error. Always returned.
status | int | The HTTP status code, if available.
url | string | A URL for more information, if available. 




## CrowdTangle Error Codes

Code | Description
-----|------------
20 | Unknown Parameter
21 | Illegal Parameter Value
22 | Missing Parameter
30 | Missing Token
31 | Invalid Token
40 | Does Not Exist
41 | Not Allowed
