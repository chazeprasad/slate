## Delete a Specific Email Alert Settings

```javascript
const http = require('http');

const headers = [] 
headers.push({ Accept: "application/vnd.alertizen+json;version=1;" } ); 
headers.push({ Authorization: "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9" } ); 

const url = "https://alertizen.herokuapp.com/api/email-alerts/1"
http.delete(url);
```


```swift
let url = URL(string: "https://alertsizen.herokuapp.com/api/email-alerts/1")
var urlRequest = URLRequest(url: url)
urlRequest.httpMethod = HTTPMethod.delete.rawValue

var headers: HTTPHeaders = HTTPHeaders()
headers["Accept"] = "application/vnd.alertizen+json;version=1;"
headers["Authorization"] = "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9"
urlRequest.allHTTPHeaderFields = headers

let request = Alamofire.request(urlRequest).responseJSON { response in
      print(response)
}
```


```shell
curl https://alertizen.herokuapp.com/api/email-alerts/1
  -H "Accept: application/vnd.alertizen+json;version=1;"
  -H "Authorization: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9"
  -X DELETE
```


> The above command returns JSON structured like this:

```json
{

}
```

This endpoint deletes a specific Email Alert Settings.

### HTTP Request

`DELETE https://alertizen.herokuapp.com/api/email-alerts/<ID>`

### URL Parameters

Parameter | Required | Description
--------- | ------- | -----------
ID | Required | The ID of the Email Alert Settings to delete.




<aside class="success">
Remember — On success you will be able to delete a specific Email Alert Settings by ID
</aside>

