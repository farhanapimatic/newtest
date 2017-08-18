# 

Simple calculator API hosted on APIMATIC



## Base URL

The Base URL for this API is `http://examples.apimatic.io/apps/calculator`



## Authentication
This API uses `OAuth v2.0` with `bearer token`.



### Authentication Parameters

The parameters required for authentication are listed below:

| Parameter | Description | Example | 
|-----------|-------------| ------- |
| new | TODO: add a description | `"new"` |
| new1 | TODO: add a description | `"new1"` |





# <a name="api_reference"></a>API Reference

* [API](#api)
* [Simple Calculator](#simple_calculator)

## <a name="api"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "API") API


### <a name="new"></a>![Endpoint: ](https://apidocs.io/img/method.png "new") new


**`POST`** `/1.1/test.php`

> TODO: Add a method description


#### Base URL
This endpoint uses server ``.


#### Request Headers
>Accept=application/json;
>Content-Type=application/json;
>cache-control="cache-control";
>content-type="content-type";
>postman-token="postman-token";

#### Request Body
Raw 

|  Type | Tags | Description |
| ------| ---- |-------------| 
| [new Request](#new_request) |  ``` Required ```  | TODO: Add description | 

 Example 
``` 
{
  "counter": 54,
  "DATA": {
    "latitude": 54.0991746909447,
    "longitude": 54.0991746909447
  }
}
``` 

#### Responses
**200** 


Body


[Back to API Reference](#api_reference)

## <a name="simple_calculator"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "Simple Calculator") Simple Calculator


### <a name="calculate"></a>![Endpoint: ](https://apidocs.io/img/method.png "Calculate") Calculate


**`GET`** `/{operation}`

> Calculates the expression using the specified operation.




#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ----------------------------------- |
| operation | [Operation Type](#operation_type) |  ``` Required ```  | The operator to apply on the variables | `MULTIPLY` | 

#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| -------------------------------- |
| x | [precision](#api_types) |  ``` Required ```  | The LHS value | `4` | 
| y | [precision](#api_types) |  ``` Required ```  | The RHS value | `5` | 

#### Responses
**200** 


Body ([Precision](#api_types)) 
```
20
```


[Back to API Reference](#api_reference)

## <a name="api_types"></a>![Models: ](https://apidocs.io/img/class.png "API Types") API Types

This section provides details on the available types. The primitive types available are:

| Type | Example |
| ---- | -------- |
| **string** | `hello world` |
| **boolean** |	`true` |
| **number** | `1` |
| **precision** | `1.5` |
| **datetime** | `2016-03-13T12:52:32.123Z` |
| **date** | `2016-03-13` |
|**void** | |
| **dynamic** | |
| **binary** | |
| **long** | `12345678910` |
| **file** | |
| **uuid** | `0f8fad5b-d9cb-469f-a165-70867728950e` |


In addition to the above types, the following complex types are also available:
### <a name="advance"></a>![Model: ](https://apidocs.io/img/method.png "Advance") Advance



> TODO: Add a method description




| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| latitude | [precision](#api_types) |  ``` Required ```  | TODO: Add a property description | 
| longitude | [precision](#api_types) |  ``` Required ```  | TODO: Add a property description | 




### <a name="new"></a>![Model: ](https://apidocs.io/img/method.png "new") new



> TODO: Add a method description




| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| counter | [number](#api_types) |  ``` Required ```  | TODO: Add a property description | 
| advance | [Advance](#advance) |  ``` Required ```  | TODO: Add a property description | 




### <a name="data"></a>![Model: ](https://apidocs.io/img/method.png "DATA") DATA



> TODO: Add a method description




| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| latitude | [precision](#api_types) |  ``` Required ```  | TODO: Add a property description | 
| longitude | [precision](#api_types) |  ``` Required ```  | TODO: Add a property description | 




### <a name="new_request"></a>![Model: ](https://apidocs.io/img/method.png "new Request") new Request



> TODO: Add a method description




| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| counter | [number](#api_types) |  ``` Required ```  | TODO: Add a property description | 
| DATA | [DATA](#data) |  ``` Required ```  | TODO: Add a property description | 




### <a name="operation_type"></a>![Model: ](https://apidocs.io/img/method.png "Operation Type") Operation Type



> Possible operators are sum, subtract, multiply, divide




This type must take a value from the following [string](#api_types) enumeration of values:

| Value | Description |
| ----- | --------------- |
| `SUM` | Represents the sum operator | 
| `SUBTRACT` | Represents the subtract operator | 
| `MULTIPLY` | Represents the multiply operator | 
| `DIVIDE` | Represents the divide operator |

