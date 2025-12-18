# V1ContentRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url** | **str** | The content URL. Must be relative and start with a leading &#39;/&#39; | 
**content** | **str** | The content (e.g. html) | 
**published** | **bool** | If the asset should be published | 
**content_timestamp** | **int** | User defined timestamp for this content item | [optional] 
**info** | [**V1Info**](V1Info.md) |  | [optional] 
**transitions** | [**List[V1Transition]**](V1Transition.md) |  | [optional] 

## Example

```python
from quantcdn.models.v1_content_request import V1ContentRequest

# TODO update the JSON string below
json = "{}"
# create an instance of V1ContentRequest from a JSON string
v1_content_request_instance = V1ContentRequest.from_json(json)
# print the JSON string representation of the object
print(V1ContentRequest.to_json())

# convert the object into a dict
v1_content_request_dict = v1_content_request_instance.to_dict()
# create an instance of V1ContentRequest from a dict
v1_content_request_from_dict = V1ContentRequest.from_dict(v1_content_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


