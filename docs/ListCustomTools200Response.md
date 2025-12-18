# ListCustomTools200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tools** | [**List[ListCustomTools200ResponseToolsInner]**](ListCustomTools200ResponseToolsInner.md) |  | [optional] 
**count** | **int** |  | [optional] 

## Example

```python
from quantcdn.models.list_custom_tools200_response import ListCustomTools200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ListCustomTools200Response from a JSON string
list_custom_tools200_response_instance = ListCustomTools200Response.from_json(json)
# print the JSON string representation of the object
print(ListCustomTools200Response.to_json())

# convert the object into a dict
list_custom_tools200_response_dict = list_custom_tools200_response_instance.to_dict()
# create an instance of ListCustomTools200Response from a dict
list_custom_tools200_response_from_dict = ListCustomTools200Response.from_dict(list_custom_tools200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


