# Markets

## Get All Markets

```javascript
const http = require('http');

const headers = []
headers.push({ Accept: "application/vnd.alertizen+json;version=1;" } ); 
headers.push({ Authorization: "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9" } ); 

const url = "https://alertizen.herokuapp.com/api/markets"
http.get(url);
```


```swift
let url = URL(string: "https://alertsizen.herokuapp.com/api/markets")
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
curl https://alertizen.herokuapp.com/api/markets
  -H "Accept: application/vnd.alertizen+json;version=1;"
  -H "Authorization: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9"
  -X GET
```

> The above command returns JSON structured like this:

```json
[
    {
        "id": 1,
        "market_name": "market 1",
        "area_type": "market",
        "vertices": "POLYGON ((40.7566484549725 -73.9878561496734, 40.7556894646734 -73.9853026866913, 40.7545841705587 -73.9860537052154, 40.7548036054111 -73.9881458282471, 40.7559820394514 -73.9887895584106, 40.7566484549725 -73.9878561496734))",
        "created_at": "2018-10-20T15:01:22.505Z",
        "updated_at": "2018-10-20T15:01:22.505Z"
    },
    {
        "id": 2,
        "market_name": "market 2",
        "area_type": "market",
        "vertices": "POLYGON ((40.7566484549725 -73.9878561496734, 40.7556894646734 -73.9853026866913, 40.7545841705587 -73.9860537052154, 40.7548036054111 -73.9881458282471, 40.7559820394514 -73.9887895584106, 40.7566484549725 -73.9878561496734))",
        "created_at": "2018-10-20T15:01:22.505Z",
        "updated_at": "2018-10-20T15:01:22.505Z"
    },
    {
        "id": 3,
        "market_name": "market 3",
        "area_type": "market",
        "vertices": "POLYGON ((40.7566484549725 -73.9878561496734, 40.7556894646734 -73.9853026866913, 40.7545841705587 -73.9860537052154, 40.7548036054111 -73.9881458282471, 40.7559820394514 -73.9887895584106, 40.7566484549725 -73.9878561496734))",
        "created_at": "2018-10-20T15:01:22.505Z",
        "updated_at": "2018-10-20T15:01:22.505Z"
    }
]
```

This endpoint retrieves all Markets.

### HTTP Request

`GET https://alertizen.herokuapp.com/api/markets`

