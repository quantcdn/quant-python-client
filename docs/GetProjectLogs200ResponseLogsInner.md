# GetProjectLogs200ResponseLogsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**timestamp** | **datetime** |  | [optional] 
**project** | **str** |  | [optional] 
**domain** | **str** |  | [optional] 
**method** | **str** |  | [optional] 
**uri** | **str** |  | [optional] 
**status_code** | **int** |  | [optional] 
**cache_status** | **str** |  | [optional] 
**client_ip** | **str** |  | [optional] 
**user_agent** | **str** |  | [optional] 
**bytes** | **int** |  | [optional] 
**time_taken** | **float** |  | [optional] 

## Example

```python
from quantcdn.models.get_project_logs200_response_logs_inner import GetProjectLogs200ResponseLogsInner

# TODO update the JSON string below
json = "{}"
# create an instance of GetProjectLogs200ResponseLogsInner from a JSON string
get_project_logs200_response_logs_inner_instance = GetProjectLogs200ResponseLogsInner.from_json(json)
# print the JSON string representation of the object
print(GetProjectLogs200ResponseLogsInner.to_json())

# convert the object into a dict
get_project_logs200_response_logs_inner_dict = get_project_logs200_response_logs_inner_instance.to_dict()
# create an instance of GetProjectLogs200ResponseLogsInner from a dict
get_project_logs200_response_logs_inner_from_dict = GetProjectLogs200ResponseLogsInner.from_dict(get_project_logs200_response_logs_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


