# CreateApplicationRequestEnvironmentInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | Environment variable name | [optional] 
**value** | **str** | Environment variable value | [optional] 

## Example

```python
from quantcdn.models.create_application_request_environment_inner import CreateApplicationRequestEnvironmentInner

# TODO update the JSON string below
json = "{}"
# create an instance of CreateApplicationRequestEnvironmentInner from a JSON string
create_application_request_environment_inner_instance = CreateApplicationRequestEnvironmentInner.from_json(json)
# print the JSON string representation of the object
print(CreateApplicationRequestEnvironmentInner.to_json())

# convert the object into a dict
create_application_request_environment_inner_dict = create_application_request_environment_inner_instance.to_dict()
# create an instance of CreateApplicationRequestEnvironmentInner from a dict
create_application_request_environment_inner_from_dict = CreateApplicationRequestEnvironmentInner.from_dict(create_application_request_environment_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


