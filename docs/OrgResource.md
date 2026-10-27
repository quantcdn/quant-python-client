# OrgResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**org_name** | **str** |  | [optional] 
**resource_id** | **str** |  | [optional] 
**type** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**status** | **str** |  | [optional] 
**scope** | **str** | org for resources managed by these endpoints. app rows are compatibility records for an application-managed cache and cannot be mutated here. | [optional] 
**config** | **object** | Type-specific settings, such as dataStorageMaxGb for a cache | [optional] 
**physical** | **object** | Provisioned detail: bucket and region for object storage, cache identifier and endpoint for a cache | [optional] 
**created_at** | **datetime** |  | [optional] 

## Example

```python
from quantcdn.models.org_resource import OrgResource

# TODO update the JSON string below
json = "{}"
# create an instance of OrgResource from a JSON string
org_resource_instance = OrgResource.from_json(json)
# print the JSON string representation of the object
print(OrgResource.to_json())

# convert the object into a dict
org_resource_dict = org_resource_instance.to_dict()
# create an instance of OrgResource from a dict
org_resource_from_dict = OrgResource.from_dict(org_resource_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


