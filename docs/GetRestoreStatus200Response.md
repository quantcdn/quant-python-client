# GetRestoreStatus200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**restore_id** | **str** |  | [optional] 
**org_name** | **str** |  | [optional] 
**app_name** | **str** |  | [optional] 
**env_name** | **str** |  | [optional] 
**backup_id** | **str** |  | [optional] 
**status** | **str** |  | [optional] 
**started_at** | **datetime** |  | [optional] 
**completed_at** | **datetime** |  | [optional] 
**error_message** | **str** |  | [optional] 
**task_arn** | **str** |  | [optional] 
**ttl** | **int** |  | [optional] 

## Example

```python
from quantcdn.models.get_restore_status200_response import GetRestoreStatus200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetRestoreStatus200Response from a JSON string
get_restore_status200_response_instance = GetRestoreStatus200Response.from_json(json)
# print the JSON string representation of the object
print(GetRestoreStatus200Response.to_json())

# convert the object into a dict
get_restore_status200_response_dict = get_restore_status200_response_instance.to_dict()
# create an instance of GetRestoreStatus200Response from a dict
get_restore_status200_response_from_dict = GetRestoreStatus200Response.from_dict(get_restore_status200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


