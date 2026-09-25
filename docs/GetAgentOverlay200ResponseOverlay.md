# GetAgentOverlay200ResponseOverlay


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**model_id** | **str** |  | [optional] 
**temperature** | **float** |  | [optional] 
**max_tokens** | **int** |  | [optional] 
**disabled_skills** | **List[str]** |  | [optional] 
**additional_skills** | **List[str]** |  | [optional] 
**additional_tools** | **List[str]** |  | [optional] 
**disabled_tools** | **List[str]** |  | [optional] 
**system_prompt_append** | **str** |  | [optional] 
**allowed_collections** | **List[str]** |  | [optional] 
**guardrail_preset** | **str** |  | [optional] 
**version** | **int** |  | [optional] 

## Example

```python
from quantcdn.models.get_agent_overlay200_response_overlay import GetAgentOverlay200ResponseOverlay

# TODO update the JSON string below
json = "{}"
# create an instance of GetAgentOverlay200ResponseOverlay from a JSON string
get_agent_overlay200_response_overlay_instance = GetAgentOverlay200ResponseOverlay.from_json(json)
# print the JSON string representation of the object
print(GetAgentOverlay200ResponseOverlay.to_json())

# convert the object into a dict
get_agent_overlay200_response_overlay_dict = get_agent_overlay200_response_overlay_instance.to_dict()
# create an instance of GetAgentOverlay200ResponseOverlay from a dict
get_agent_overlay200_response_overlay_from_dict = GetAgentOverlay200ResponseOverlay.from_dict(get_agent_overlay200_response_overlay_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


