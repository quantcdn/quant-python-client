# CreateCommandRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**command** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.create_command_request import CreateCommandRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateCommandRequest from a JSON string
create_command_request_instance = CreateCommandRequest.from_json(json)
# print the JSON string representation of the object
print(CreateCommandRequest.to_json())

# convert the object into a dict
create_command_request_dict = create_command_request_instance.to_dict()
# create an instance of CreateCommandRequest from a dict
create_command_request_from_dict = CreateCommandRequest.from_dict(create_command_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


