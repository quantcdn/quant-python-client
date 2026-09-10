# CreateOrgResourceRequestConfig

Valkey only

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**data_storage_max_gb** | **int** |  | [optional] 

## Example

```python
from quantcdn.models.create_org_resource_request_config import CreateOrgResourceRequestConfig

# TODO update the JSON string below
json = "{}"
# create an instance of CreateOrgResourceRequestConfig from a JSON string
create_org_resource_request_config_instance = CreateOrgResourceRequestConfig.from_json(json)
# print the JSON string representation of the object
print(CreateOrgResourceRequestConfig.to_json())

# convert the object into a dict
create_org_resource_request_config_dict = create_org_resource_request_config_instance.to_dict()
# create an instance of CreateOrgResourceRequestConfig from a dict
create_org_resource_request_config_from_dict = CreateOrgResourceRequestConfig.from_dict(create_org_resource_request_config_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


