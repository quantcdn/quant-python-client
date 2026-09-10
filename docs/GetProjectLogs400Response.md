# GetProjectLogs400Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**error** | **bool** |  | [optional] 
**message** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.get_project_logs400_response import GetProjectLogs400Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetProjectLogs400Response from a JSON string
get_project_logs400_response_instance = GetProjectLogs400Response.from_json(json)
# print the JSON string representation of the object
print(GetProjectLogs400Response.to_json())

# convert the object into a dict
get_project_logs400_response_dict = get_project_logs400_response_instance.to_dict()
# create an instance of GetProjectLogs400Response from a dict
get_project_logs400_response_from_dict = GetProjectLogs400Response.from_dict(get_project_logs400_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


