# GetProjectEdgeEvents200ResponseEventsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**timestamp** | **datetime** |  | [optional] 
**type** | **str** |  | [optional] 
**level** | **str** |  | [optional] 
**function_uuid** | **str** |  | [optional] 
**message** | **str** |  | [optional] 
**truncated** | **bool** |  | [optional] 
**host** | **str** |  | [optional] 
**path** | **str** |  | [optional] 
**client_ip** | **str** |  | [optional] 
**rule_id** | **str** |  | [optional] 
**waf_mode** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.get_project_edge_events200_response_events_inner import GetProjectEdgeEvents200ResponseEventsInner

# TODO update the JSON string below
json = "{}"
# create an instance of GetProjectEdgeEvents200ResponseEventsInner from a JSON string
get_project_edge_events200_response_events_inner_instance = GetProjectEdgeEvents200ResponseEventsInner.from_json(json)
# print the JSON string representation of the object
print(GetProjectEdgeEvents200ResponseEventsInner.to_json())

# convert the object into a dict
get_project_edge_events200_response_events_inner_dict = get_project_edge_events200_response_events_inner_instance.to_dict()
# create an instance of GetProjectEdgeEvents200ResponseEventsInner from a dict
get_project_edge_events200_response_events_inner_from_dict = GetProjectEdgeEvents200ResponseEventsInner.from_dict(get_project_edge_events200_response_events_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


