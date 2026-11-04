# ListAIAgents200ResponseAgentsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**agent_id** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**group** | **str** |  | [optional] 
**model_id** | **str** |  | [optional] 
**temperature** | **float** |  | [optional] 
**max_tokens** | **int** |  | [optional] 
**allowed_tools** | **List[str]** |  | [optional] 
**assigned_skills** | **List[str]** |  | [optional] 
**long_context** | **bool** |  | [optional] 
**reasoning_effort** | **str** | Reasoning effort (Anthropic effort). Must be one of the levels the model lists in capabilities.effortLevels. Unset uses the caller or model default. | [optional] 
**guardrail_preset** | **str** |  | [optional] 
**filter_policies** | **List[str]** | Filter policy IDs applied to this agent&#39;s requests (organisation agents) | [optional] 
**mcp_servers** | [**List[ListAIAgents200ResponseAgentsInnerMcpServersInner]**](ListAIAgents200ResponseAgentsInnerMcpServersInner.md) | Attached MCP servers. A platform agent shows its organisation overlay&#39;s attachments. | [optional] 
**is_global** | **bool** |  | [optional] 
**has_overlay** | **bool** |  | [optional] 
**created_at** | **datetime** |  | [optional] 
**updated_at** | **datetime** |  | [optional] 

## Example

```python
from quantcdn.models.list_ai_agents200_response_agents_inner import ListAIAgents200ResponseAgentsInner

# TODO update the JSON string below
json = "{}"
# create an instance of ListAIAgents200ResponseAgentsInner from a JSON string
list_ai_agents200_response_agents_inner_instance = ListAIAgents200ResponseAgentsInner.from_json(json)
# print the JSON string representation of the object
print(ListAIAgents200ResponseAgentsInner.to_json())

# convert the object into a dict
list_ai_agents200_response_agents_inner_dict = list_ai_agents200_response_agents_inner_instance.to_dict()
# create an instance of ListAIAgents200ResponseAgentsInner from a dict
list_ai_agents200_response_agents_inner_from_dict = ListAIAgents200ResponseAgentsInner.from_dict(list_ai_agents200_response_agents_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


