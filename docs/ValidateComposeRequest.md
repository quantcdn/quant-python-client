# ValidateComposeRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**compose** | **str** | The docker-compose.yml file content as a string | 
**image_suffix** | **str** | Optional image tag suffix (query parameter takes precedence) | [optional] 
**application** | **str** | Optional application name for context | [optional] 

## Example

```python
from quantcdn.models.validate_compose_request import ValidateComposeRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ValidateComposeRequest from a JSON string
validate_compose_request_instance = ValidateComposeRequest.from_json(json)
# print the JSON string representation of the object
print(ValidateComposeRequest.to_json())

# convert the object into a dict
validate_compose_request_dict = validate_compose_request_instance.to_dict()
# create an instance of ValidateComposeRequest from a dict
validate_compose_request_from_dict = ValidateComposeRequest.from_dict(validate_compose_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


