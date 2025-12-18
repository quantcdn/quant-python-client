# GetSshAccessCredentials200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**credentials** | [**GetSshAccessCredentials200ResponseCredentials**](GetSshAccessCredentials200ResponseCredentials.md) |  | [optional] 
**cluster_name** | **str** |  | [optional] 
**task_arn** | **str** |  | [optional] 
**task_id** | **str** |  | [optional] 
**container_names** | **List[str]** |  | [optional] 
**region** | **str** |  | [optional] 
**expires_in** | **int** |  | [optional] 
**organization_scope** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.get_ssh_access_credentials200_response import GetSshAccessCredentials200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetSshAccessCredentials200Response from a JSON string
get_ssh_access_credentials200_response_instance = GetSshAccessCredentials200Response.from_json(json)
# print the JSON string representation of the object
print(GetSshAccessCredentials200Response.to_json())

# convert the object into a dict
get_ssh_access_credentials200_response_dict = get_ssh_access_credentials200_response_instance.to_dict()
# create an instance of GetSshAccessCredentials200Response from a dict
get_ssh_access_credentials200_response_from_dict = GetSshAccessCredentials200Response.from_dict(get_ssh_access_credentials200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


