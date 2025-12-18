# BulkSetEnvironmentVariablesRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**environment** | [**List[BulkSetEnvironmentVariablesRequestEnvironmentInner]**](BulkSetEnvironmentVariablesRequestEnvironmentInner.md) |  | 

## Example

```python
from quantcdn.models.bulk_set_environment_variables_request import BulkSetEnvironmentVariablesRequest

# TODO update the JSON string below
json = "{}"
# create an instance of BulkSetEnvironmentVariablesRequest from a JSON string
bulk_set_environment_variables_request_instance = BulkSetEnvironmentVariablesRequest.from_json(json)
# print the JSON string representation of the object
print(BulkSetEnvironmentVariablesRequest.to_json())

# convert the object into a dict
bulk_set_environment_variables_request_dict = bulk_set_environment_variables_request_instance.to_dict()
# create an instance of BulkSetEnvironmentVariablesRequest from a dict
bulk_set_environment_variables_request_from_dict = BulkSetEnvironmentVariablesRequest.from_dict(bulk_set_environment_variables_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


