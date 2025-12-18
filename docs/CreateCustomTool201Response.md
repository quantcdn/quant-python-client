# CreateCustomTool201Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**tool** | **object** |  | [optional] 
**message** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.create_custom_tool201_response import CreateCustomTool201Response

# TODO update the JSON string below
json = "{}"
# create an instance of CreateCustomTool201Response from a JSON string
create_custom_tool201_response_instance = CreateCustomTool201Response.from_json(json)
# print the JSON string representation of the object
print(CreateCustomTool201Response.to_json())

# convert the object into a dict
create_custom_tool201_response_dict = create_custom_tool201_response_instance.to_dict()
# create an instance of CreateCustomTool201Response from a dict
create_custom_tool201_response_from_dict = CreateCustomTool201Response.from_dict(create_custom_tool201_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


