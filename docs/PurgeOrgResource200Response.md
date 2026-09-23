# PurgeOrgResource200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**scope** | **str** |  | [optional] 
**prefix** | **str** |  | [optional] 
**deleted_keys** | **int** |  | [optional] 
**complete** | **bool** |  | [optional] 
**cursor** | **str** |  | [optional] 
**flushed** | **bool** |  | [optional] 

## Example

```python
from quantcdn.models.purge_org_resource200_response import PurgeOrgResource200Response

# TODO update the JSON string below
json = "{}"
# create an instance of PurgeOrgResource200Response from a JSON string
purge_org_resource200_response_instance = PurgeOrgResource200Response.from_json(json)
# print the JSON string representation of the object
print(PurgeOrgResource200Response.to_json())

# convert the object into a dict
purge_org_resource200_response_dict = purge_org_resource200_response_instance.to_dict()
# create an instance of PurgeOrgResource200Response from a dict
purge_org_resource200_response_from_dict = PurgeOrgResource200Response.from_dict(purge_org_resource200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


