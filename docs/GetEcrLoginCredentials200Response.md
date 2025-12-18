# GetEcrLoginCredentials200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**username** | **str** |  | [optional] 
**password** | **str** |  | [optional] 
**expires_at** | **str** |  | [optional] 
**endpoint** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.get_ecr_login_credentials200_response import GetEcrLoginCredentials200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetEcrLoginCredentials200Response from a JSON string
get_ecr_login_credentials200_response_instance = GetEcrLoginCredentials200Response.from_json(json)
# print the JSON string representation of the object
print(GetEcrLoginCredentials200Response.to_json())

# convert the object into a dict
get_ecr_login_credentials200_response_dict = get_ecr_login_credentials200_response_instance.to_dict()
# create an instance of GetEcrLoginCredentials200Response from a dict
get_ecr_login_credentials200_response_from_dict = GetEcrLoginCredentials200Response.from_dict(get_ecr_login_credentials200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


