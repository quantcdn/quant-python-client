# GetAgentOverlay200ResponseBase

Base global agent metadata

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**agent_id** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**model_id** | **str** |  | [optional] 
**allowed_tools** | **List[str]** |  | [optional] 
**assigned_skill_ids** | **List[str]** |  | [optional] 

## Example

```python
from quantcdn.models.get_agent_overlay200_response_base import GetAgentOverlay200ResponseBase

# TODO update the JSON string below
json = "{}"
# create an instance of GetAgentOverlay200ResponseBase from a JSON string
get_agent_overlay200_response_base_instance = GetAgentOverlay200ResponseBase.from_json(json)
# print the JSON string representation of the object
print(GetAgentOverlay200ResponseBase.to_json())

# convert the object into a dict
get_agent_overlay200_response_base_dict = get_agent_overlay200_response_base_instance.to_dict()
# create an instance of GetAgentOverlay200ResponseBase from a dict
get_agent_overlay200_response_base_from_dict = GetAgentOverlay200ResponseBase.from_dict(get_agent_overlay200_response_base_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


