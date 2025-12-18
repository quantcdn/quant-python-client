# ListCustomTools200ResponseToolsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**edge_function_url** | **str** |  | [optional] 
**is_async** | **bool** |  | [optional] 
**input_schema** | **object** |  | [optional] 
**created_at** | **datetime** |  | [optional] 

## Example

```python
from quantcdn.models.list_custom_tools200_response_tools_inner import ListCustomTools200ResponseToolsInner

# TODO update the JSON string below
json = "{}"
# create an instance of ListCustomTools200ResponseToolsInner from a JSON string
list_custom_tools200_response_tools_inner_instance = ListCustomTools200ResponseToolsInner.from_json(json)
# print the JSON string representation of the object
print(ListCustomTools200ResponseToolsInner.to_json())

# convert the object into a dict
list_custom_tools200_response_tools_inner_dict = list_custom_tools200_response_tools_inner_instance.to_dict()
# create an instance of ListCustomTools200ResponseToolsInner from a dict
list_custom_tools200_response_tools_inner_from_dict = ListCustomTools200ResponseToolsInner.from_dict(list_custom_tools200_response_tools_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


