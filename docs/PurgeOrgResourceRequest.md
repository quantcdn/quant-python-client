# PurgeOrgResourceRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**scope** | **str** |  | 
**application** | **str** | scope environment only | [optional] 
**environment** | **str** | scope environment only | [optional] 
**confirm** | **bool** | scope all only; must be true | [optional] 
**cursor** | **str** | scope environment only; resume a partial purge | [optional] 

## Example

```python
from quantcdn.models.purge_org_resource_request import PurgeOrgResourceRequest

# TODO update the JSON string below
json = "{}"
# create an instance of PurgeOrgResourceRequest from a JSON string
purge_org_resource_request_instance = PurgeOrgResourceRequest.from_json(json)
# print the JSON string representation of the object
print(PurgeOrgResourceRequest.to_json())

# convert the object into a dict
purge_org_resource_request_dict = purge_org_resource_request_instance.to_dict()
# create an instance of PurgeOrgResourceRequest from a dict
purge_org_resource_request_from_dict = PurgeOrgResourceRequest.from_dict(purge_org_resource_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


