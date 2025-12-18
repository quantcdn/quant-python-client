# GetSshAccessCredentials200ResponseCredentials


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**access_key_id** | **str** |  | [optional] 
**secret_access_key** | **str** |  | [optional] 
**session_token** | **str** |  | [optional] 
**expiration** | **datetime** |  | [optional] 

## Example

```python
from quantcdn.models.get_ssh_access_credentials200_response_credentials import GetSshAccessCredentials200ResponseCredentials

# TODO update the JSON string below
json = "{}"
# create an instance of GetSshAccessCredentials200ResponseCredentials from a JSON string
get_ssh_access_credentials200_response_credentials_instance = GetSshAccessCredentials200ResponseCredentials.from_json(json)
# print the JSON string representation of the object
print(GetSshAccessCredentials200ResponseCredentials.to_json())

# convert the object into a dict
get_ssh_access_credentials200_response_credentials_dict = get_ssh_access_credentials200_response_credentials_instance.to_dict()
# create an instance of GetSshAccessCredentials200ResponseCredentials from a dict
get_ssh_access_credentials200_response_credentials_from_dict = GetSshAccessCredentials200ResponseCredentials.from_dict(get_ssh_access_credentials200_response_credentials_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


