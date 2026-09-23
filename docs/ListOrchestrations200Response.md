# ListOrchestrations200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**orchestrations** | **List[object]** |  | [optional] 
**next_cursor** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.list_orchestrations200_response import ListOrchestrations200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ListOrchestrations200Response from a JSON string
list_orchestrations200_response_instance = ListOrchestrations200Response.from_json(json)
# print the JSON string representation of the object
print(ListOrchestrations200Response.to_json())

# convert the object into a dict
list_orchestrations200_response_dict = list_orchestrations200_response_instance.to_dict()
# create an instance of ListOrchestrations200Response from a dict
list_orchestrations200_response_from_dict = ListOrchestrations200Response.from_dict(list_orchestrations200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


