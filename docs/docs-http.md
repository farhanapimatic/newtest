# 



## Base URL

The Base URL for this API is `http://Example.org/ICalculator`






# <a name="api_reference"></a>API Reference

* [DefaultBinding_ICalculator](#default_binding_i_calculator)

## <a name="default_binding_i_calculator"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "DefaultBinding_ICalculator") DefaultBinding_ICalculator


### <a name="add"></a>![Endpoint: ](https://apidocs.io/img/method.png "Add") Add


**`POST`** `/Add`

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add a method description



#### Request Headers
>Accept=application/json;
>Content-Type=application/json;

#### Request Body
Raw 

|  Type | Tags | Description |
| ------| ---- |-------------| 
| `icalculator_add_inputmessage` |  ``` Required ```  | TODO: Add a parameter description | 

 Example 
``` 
{
  "parameters": {
    "a": 106,
    "b": 106
  }
}
``` 

#### Responses
**200** 

Body (_ICalculator_Add_OutputMessage_) 
```
{
  "parameters": {
    "result": 106
  }
}
```


### <a name="subtract"></a>![Endpoint: ](https://apidocs.io/img/method.png "Subtract") Subtract


**`POST`** `/Subtract`

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add a method description



#### Request Headers
>Accept=application/json;
>Content-Type=application/json;

#### Request Body
Raw 

|  Type | Tags | Description |
| ------| ---- |-------------| 
| `icalculator_subtract_inputmessage` |  ``` Required ```  | TODO: Add a parameter description | 

 Example 
``` 
{
  "parameters": {
    "a": 64,
    "b": 64
  }
}
``` 

#### Responses
**200** 

Body (_ICalculator_Subtract_OutputMessage_) 
```
{
  "parameters": {
    "result": 64
  }
}
```


[Back to API Reference](#api_reference)

