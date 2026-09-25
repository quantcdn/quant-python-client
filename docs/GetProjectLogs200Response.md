# GetProjectLogs200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**logs** | [**List[GetProjectLogs200ResponseLogsInner]**](GetProjectLogs200ResponseLogsInner.md) | Structured CloudFront access log entries. Each entry carries request, response, timing and cache fields as emitted by the edge. | [optional] 
**count** | **int** | Number of entries in this response | [optional] 
**next_token** | **str** | Token for the next page, or null when there are no more entries | [optional] 

## Example

```python
from quantcdn.models.get_project_logs200_response import GetProjectLogs200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetProjectLogs200Response from a JSON string
get_project_logs200_response_instance = GetProjectLogs200Response.from_json(json)
# print the JSON string representation of the object
print(GetProjectLogs200Response.to_json())

# convert the object into a dict
get_project_logs200_response_dict = get_project_logs200_response_instance.to_dict()
# create an instance of GetProjectLogs200Response from a dict
get_project_logs200_response_from_dict = GetProjectLogs200Response.from_dict(get_project_logs200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


