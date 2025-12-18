# CreateApplication403Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | [optional] 
**error** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.create_application403_response import CreateApplication403Response

# TODO update the JSON string below
json = "{}"
# create an instance of CreateApplication403Response from a JSON string
create_application403_response_instance = CreateApplication403Response.from_json(json)
# print the JSON string representation of the object
print(CreateApplication403Response.to_json())

# convert the object into a dict
create_application403_response_dict = create_application403_response_instance.to_dict()
# create an instance of CreateApplication403Response from a dict
create_application403_response_from_dict = CreateApplication403Response.from_dict(create_application403_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


