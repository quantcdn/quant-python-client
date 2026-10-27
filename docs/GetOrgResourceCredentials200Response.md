# GetOrgResourceCredentials200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**host** | **str** |  | [optional] 
**port** | **int** |  | [optional] 
**tls** | **bool** |  | [optional] 
**username** | **str** |  | [optional] 
**password** | **str** |  | [optional] 
**note** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.get_org_resource_credentials200_response import GetOrgResourceCredentials200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetOrgResourceCredentials200Response from a JSON string
get_org_resource_credentials200_response_instance = GetOrgResourceCredentials200Response.from_json(json)
# print the JSON string representation of the object
print(GetOrgResourceCredentials200Response.to_json())

# convert the object into a dict
get_org_resource_credentials200_response_dict = get_org_resource_credentials200_response_instance.to_dict()
# create an instance of GetOrgResourceCredentials200Response from a dict
get_org_resource_credentials200_response_from_dict = GetOrgResourceCredentials200Response.from_dict(get_org_resource_credentials200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


