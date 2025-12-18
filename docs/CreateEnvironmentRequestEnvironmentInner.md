# CreateEnvironmentRequestEnvironmentInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | Variable name | [optional] 
**value** | **str** | Variable value | [optional] 

## Example

```python
from quantcdn.models.create_environment_request_environment_inner import CreateEnvironmentRequestEnvironmentInner

# TODO update the JSON string below
json = "{}"
# create an instance of CreateEnvironmentRequestEnvironmentInner from a JSON string
create_environment_request_environment_inner_instance = CreateEnvironmentRequestEnvironmentInner.from_json(json)
# print the JSON string representation of the object
print(CreateEnvironmentRequestEnvironmentInner.to_json())

# convert the object into a dict
create_environment_request_environment_inner_dict = create_environment_request_environment_inner_instance.to_dict()
# create an instance of CreateEnvironmentRequestEnvironmentInner from a dict
create_environment_request_environment_inner_from_dict = CreateEnvironmentRequestEnvironmentInner.from_dict(create_environment_request_environment_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


