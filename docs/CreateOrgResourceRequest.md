# CreateOrgResourceRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **str** |  | 
**name** | **str** | Lowercase letters, numbers and hyphens, 2-41 characters, starting with a letter or number | 
**config** | [**CreateOrgResourceRequestConfig**](CreateOrgResourceRequestConfig.md) |  | [optional] 

## Example

```python
from quantcdn.models.create_org_resource_request import CreateOrgResourceRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateOrgResourceRequest from a JSON string
create_org_resource_request_instance = CreateOrgResourceRequest.from_json(json)
# print the JSON string representation of the object
print(CreateOrgResourceRequest.to_json())

# convert the object into a dict
create_org_resource_request_dict = create_org_resource_request_instance.to_dict()
# create an instance of CreateOrgResourceRequest from a dict
create_org_resource_request_from_dict = CreateOrgResourceRequest.from_dict(create_org_resource_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


