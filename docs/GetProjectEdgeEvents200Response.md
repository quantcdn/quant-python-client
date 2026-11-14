# GetProjectEdgeEvents200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**events** | [**List[GetProjectEdgeEvents200ResponseEventsInner]**](GetProjectEdgeEvents200ResponseEventsInner.md) |  | [optional] 
**count** | **int** |  | [optional] 
**next_token** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.get_project_edge_events200_response import GetProjectEdgeEvents200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetProjectEdgeEvents200Response from a JSON string
get_project_edge_events200_response_instance = GetProjectEdgeEvents200Response.from_json(json)
# print the JSON string representation of the object
print(GetProjectEdgeEvents200Response.to_json())

# convert the object into a dict
get_project_edge_events200_response_dict = get_project_edge_events200_response_instance.to_dict()
# create an instance of GetProjectEdgeEvents200Response from a dict
get_project_edge_events200_response_from_dict = GetProjectEdgeEvents200Response.from_dict(get_project_edge_events200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


