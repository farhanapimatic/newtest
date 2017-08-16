# 

TODO: Add a description



## Base URL

The Base URL for this API is `https://api.example.com`



## Authentication
This API uses `OAuth v2.0` with `bearer token`.






# <a name="api_reference"></a>API Reference

* [Notes](#notes)
* [Users](#users)
* [Tags and Tagging Long Title](#tags_and_tagging_long_title)

## <a name="notes"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "Notes") Notes


### <a name="get_notes"></a>![Endpoint: ](https://apidocs.io/img/method.png "Get Notes") Get Notes


**`GET`** `/notes`

> Get a list of notes.




#### Responses
**200** 


Body ([NoteData](#note_data)) 
```
[
  {
    "id": 1,
    "title": "Grocery list",
    "body": "Buy milk"
  }
]
```


### <a name="create_new_note"></a>![Endpoint: ](https://apidocs.io/img/method.png "Create New Note") Create New Note


**`POST`** `/notes`

> Create a new note using a title and an optional content body.




#### Request Headers
>Accept=application/json;
>Content-Type=application/json;

#### Request Body
Raw 

|  Type | Tags | Description |
| ------| ---- |-------------| 
| [Create New Note request](#create_new_note_request) |  ``` Required ```  | TODO: Add description | 

 Example 
``` 
{
  "title": "My new note",
  "body": "This is the body"
}
``` 

#### Responses
**200** 



**400** 

> Unexpected error in API call. See HTTP response body for details.


### <a name="get_note"></a>![Endpoint: ](https://apidocs.io/img/method.png "Get Note") Get Note


**`GET`** `/notes/{id}`

> Get a single note.




#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ----------------------------------- |
| id | [string](#api_types) |  ``` Required ```  | The note ID | `68a5sdf67` | 

#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| -------------------------------- |
| body | [boolean](#api_types) |  ``` Required ```  | Set to `false` to exclude note body content. | `false` | 

#### Responses
**200** 


Body ([NoteData](#note_data)) 
```
{
  "id": 1,
  "title": "Grocery list",
  "body": "Buy milk"
}
```


**404** 

> Unexpected error in API call. See HTTP response body for details.


### <a name="update_a_note"></a>![Endpoint: ](https://apidocs.io/img/method.png "Update a Note") Update a Note


**`PUT`** `/notes/{id}`

> Update a single note by setting the title and/or body.
> ::: warning
> #### <i class="fa fa-warning"></i> Caution
> If the value for `title` or `body` is `null` or `undefined`, then the corresponding value is not modified on the server. However, if you send an empty string instead then it will **permanently overwrite** the original value.
> :::




#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ----------------------------------- |
| id | [string](#api_types) |  ``` Required ```  | The note ID | `68a5sdf67` | 

#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| -------------------------------- |
| body | [string](#api_types) |  ``` Optional ```  | TODO: Add a parameter description | `"body"` | 

#### Responses
**200** 


Body ([NoteData](#note_data)) 
```
{
  "id": 1,
  "title": "Grocery list",
  "body": "Buy milk"
}
```


**404** 

> Unexpected error in API call. See HTTP response body for details.


### <a name="delete_a_note"></a>![Endpoint: ](https://apidocs.io/img/method.png "Delete a Note") Delete a Note


**`DELETE`** `/notes/{id}`

> Delete a single note




#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ----------------------------------- |
| id | [string](#api_types) |  ``` Required ```  | The note ID | `68a5sdf67` | 

#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| -------------------------------- |
| body | [string](#api_types) |  ``` Optional ```  | TODO: Add a parameter description | `"body"` | 

#### Responses
**200** 



**404** 

> Unexpected error in API call. See HTTP response body for details.


[Back to API Reference](#api_reference)

## <a name="users"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "Users") Users


### <a name="get_users"></a>![Endpoint: ](https://apidocs.io/img/method.png "Get users") Get users


**`GET`** `/users`

> Get a list of users. Example:
> ```no-highlight
> https://api.mywebsite.com/users?sort=joined&limit=5
> ```




#### Query Parameters
| Parameter | Type | Tags | Description | Example/Default |
|-----------|------| ---- |-------------| -------------------------------- |
| name | [string](#api_types) |  ``` Optional ```  | Search for a user by name | `alice` | 
| joinedBefore | [string](#api_types) |  ``` Optional ```  | Search by join date | `2011-01-01` | 
| joinedAfter | [string](#api_types) |  ``` Optional ```  | Search by join date | `2011-01-01` | 
| sort | [sort](#sort) |  ``` Optional ```  | Which field to sort by | **Default:** `"name"` | 
| limit | [number](#api_types) |  ``` Optional ```  | The maximum number of users to return, up to `50` | `25` | 

#### Responses
**200** 


Body ([Get users response](#get_users_response)) 
```
[
  {
    "name": "alice",
    "image": "http://example.com/alice.jpg",
    "joined": "2013-11-01"
  },
  {
    "name": "bob",
    "image": "http://example.com/bob.jpg",
    "joined": "2013-11-02"
  }
]
```


[Back to API Reference](#api_reference)

## <a name="tags_and_tagging_long_title"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "Tags and Tagging Long Title") Tags and Tagging Long Title


### <a name="tags"></a>![Endpoint: ](https://apidocs.io/img/method.png "Tags") Tags


**`GET`** `/tags`

> Get a list of bars




#### Responses
**200** 


Body ([String](#api_types)) 
```
[
  "tag1",
  "tag2",
  "tag3"
]
```


### <a name="get_get_one_tag"></a>![Endpoint: ](https://apidocs.io/img/method.png "Get Get one tag") Get Get one tag


**`GET`** `/tags/{id}`

> Get a single tag




#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ----------------------------------- |
| id | [string](#api_types) |  ``` Required ```  | Unique tag identifier | `"id"` | 

#### Responses
**200** 


Body


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
### <a name="note_data"></a>![Model: ](https://apidocs.io/img/method.png "NoteData") NoteData



> TODO: Add a method description




| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| id | [precision](#api_types) |  ``` Required ```  | Unique identifier | 
| title | [string](#api_types) |  ``` Required ```  | Single line description | 
| body | [string](#api_types) |  ``` Optional ```  | Full description of the note which supports Markdown. | 




### <a name="create_new_note_request"></a>![Model: ](https://apidocs.io/img/method.png "Create New Note request") Create New Note request



> TODO: Add a method description




| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| title | [string](#api_types) |  ``` Required ```  | TODO: Add a property description | 
| body | [string](#api_types) |  ``` Required ```  | TODO: Add a property description | 




### <a name="create_new_note_request3"></a>![Model: ](https://apidocs.io/img/method.png "Create New Note request3") Create New Note request3



> TODO: Add a method description




| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| title | [string](#api_types) |  ``` Required ```  | TODO: Add a property description | 




### <a name="update_a_note_request"></a>![Model: ](https://apidocs.io/img/method.png "Update a Note request") Update a Note request



> TODO: Add a method description




| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| title | [string](#api_types) |  ``` Required ```  | TODO: Add a property description | 




### <a name="update_a_note_request7"></a>![Model: ](https://apidocs.io/img/method.png "Update a Note request7") Update a Note request7



> TODO: Add a method description




| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| body | [string](#api_types) |  ``` Required ```  | TODO: Add a property description | 




### <a name="sort"></a>![Model: ](https://apidocs.io/img/method.png "sort") sort



> TODO: Add a method description




This type must take a value from the following [string](#api_types) enumeration of values:

| Value | Description |
| ----- | --------------- |
| `name` | TODO: Add description | 
| `joined` | TODO: Add description | 
| `-joined` | TODO: Add description | 
| `age` | TODO: Add description | 
| `-age` | TODO: Add description | 
| `location` | TODO: Add description | 
| `-location` | TODO: Add description | 
| `plan` | TODO: Add description | 
| `-plan` | TODO: Add description | 




### <a name="get_users_response"></a>![Model: ](https://apidocs.io/img/method.png "Get users response") Get users response



> TODO: Add a method description




| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| name | [string](#api_types) |  ``` Required ```  | TODO: Add a property description | 
| image | [string](#api_types) |  ``` Required ```  | TODO: Add a property description | 
| joined | [string](#api_types) |  ``` Required ```  | TODO: Add a property description |

