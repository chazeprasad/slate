## Get a Specific Email Alerts Settings

```javascript
const http = require('http');

const headers = [] 
headers.push({ Accept: "application/vnd.alertizen+json;version=1;" } ); 
headers.push({ Authorization: "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9" } ); 

const url = "https://alertizen.herokuapp.com/api/mobile-alerts/1"
http.get(url);
```


```swift
let url = URL(string: "https://alertsizen.herokuapp.com/api/mobile-alerts/1")
var urlRequest = URLRequest(url: url)
urlRequest.httpMethod = HTTPMethod.get.rawValue

var headers: HTTPHeaders = HTTPHeaders()
headers["Accept"] = "application/vnd.alertizen+json;version=1;"
headers["Authorization"] = "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9"
urlRequest.allHTTPHeaderFields = headers

let request = Alamofire.request(urlRequest).responseJSON { response in
      print(response)
}
```


```shell
curl https://alertizen.herokuapp.com/api/mobile-alerts/1
  -H "Accept: application/vnd.alertizen+json;version=1;"
  -H "Authorization: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9"
  -X GET
```


> The above command returns JSON structured like this:

```json
{
    "id": 1,
    "is_active": true,
    "device_token": "11112222333344441111222233334444",
    "os_name": "iOS",
    "os_version": "11.1",
    "owner": "1",
    "created_at": "2018-10-20T14:27:37.891Z",
    "updated_at": "2018-10-20T14:27:37.891Z"
}
```

This endpoint retrieves a specific Email Alerts Settings.

### HTTP Request

`GET https://alertizen.herokuapp.com/api/mobile-alerts/<ID>`

### URL Parameters

Parameter | Required | Description
--------- | ------- | -----------
ID | Required | The ID of the Email Alerts Settings to find.




<aside class="success">
Remember — On success you will get a specific Email Alert Settings by ID
</aside>
