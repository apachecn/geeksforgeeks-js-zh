# 使用 JavaScript 中的 APIs】

> 原文:[https://www . geesforgeks . org/work-with-API-in-JavaScript/](https://www.geeksforgeeks.org/working-with-apis-in-javascript/)

[应用编程接口](https://www.geeksforgeeks.org/introduction-to-apis/)只是一个在接口之间获取或发送数据的媒介。假设您想创建一个应用程序，为用户提供从服务器获取的一些实时数据，或者甚至允许您修改数据或将数据添加到其他端点。这是由应用编程接口或应用编程接口实现的。

我们将使用一个简单的公共应用编程接口，它不需要身份验证，允许您通过使用 **GET** 请求查询应用编程接口来获取一些数据。

[https://randomuser.me/](https://randomuser.me/)是一个为随机用户提供虚拟数据的网站，我们可以轻松使用。我们可以通过向[https://randomuser.me/api/](https://randomuser.me/api/)提出请求来获得响应。我们收到的 [JSON](https://www.geeksforgeeks.org/javascript-json/) 回复的格式如下。

## Javascript

```html
{
    "results": [
        {
            "gender": "female",
            "name": {
                "title": "Miss",
                "first": "Nina",
                "last": "Simmmons"
            },
            "location": {
                "street": {
                    "number": 970,
                    "name": "Eason Rd"
                },
                "city": "Fullerton",
                "state": "Wyoming",
                "country": "United States",
                "postcode": 57089,
                "coordinates": {
                    "latitude": "83.1807",
                    "longitude": "104.7170"
                },
                "timezone": {
                    "offset": "+8:00",
                    "description":
        "Beijing, Perth, Singapore, Hong Kong"
                }
            },
            "email": "nina.simmmons@example.com",
            "login": {
                "uuid": "bd0d135f-84df-4102-aa4f-5baaa41baf5c",
                "username": "yellowfrog722",
                "password": "dawg",
                "salt": "q28gdiyN",
                "md5": "291987daea22bb91775226574925b271",
                "sha1": "a0463a26ea5c2ff4f3ad498fd01c5994926e5021",
                "sha256":
"6583eb74ca08bfac50b3b29aa52c9f02ea5d9d017fef0e5a5a6fae4f5225f928"
            },
            "dob": {
                "date": "1980-11-01T23:10:05.403Z",
                "age": 40
            },
            "registered": {
                "date": "2013-04-02T02:26:52.904Z",
                "age": 7
            },
            "phone": "(216)-693-7015",
            "cell": "(501)-534-9413",
            "id": {
                "name": "SSN",
                "value": "847-09-2973"
            },
            "picture": {
                "large":
"https://randomuser.me/api/portraits/women/60.jpg",
                "medium":
"https://randomuser.me/api/portraits/med/women/60.jpg",
                "thumbnail":
"https://randomuser.me/api/portraits/thumb/women/60.jpg"
            },
            "nat": "US"
        }
    ],
    "info": {
        "seed": "82a8d8d4a996ba17",
        "results": 1,
        "page": 1,
        "version": "1.3"
    }
}
```