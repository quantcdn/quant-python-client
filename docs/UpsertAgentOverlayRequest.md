# UpsertAgentOverlayRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**model_id** | **str** | Override the base agent&#39;s model | [optional] 
**temperature** | **float** | Override temperature | [optional] 
**max_tokens** | **int** | Override max tokens | [optional] 
**disabled_skills** | **List[str]** | Global skill IDs to exclude | [optional] 
**additional_skills** | **List[str]** | Org-owned skill IDs to add | [optional] 
**additional_tools** | **List[str]** | Tool names to add | [optional] 
**disabled_tools** | **List[str]** | Tool names to remove | [optional] 
**system_prompt_append** | **str** | Text appended to base system prompt | [optional] 
**allowed_collections** | **List[str]** | Vector DB collections | [optional] 
**mcp_servers** | [**List[CreateAIAgentRequestMcpServersInner]**](CreateAIAgentRequestMcpServersInner.md) | Registered MCP servers to attach. The agent gets the tools of each server in dashboard chat and in QuantCode. The overlay PUT replaces the whole overlay: omit the field or send an empty array to remove every attachment. | [optional] 
**guardrail_preset** | **str** | Guardrail preset | [optional] 
**long_context** | **bool** | Force the 1M context window on (true) or off (false) for this organisation. Omit or null to use the platform default. | [optional] 
**filter_policies** | **List[str]** | Filter policy IDs applied to this agent&#39;s requests for this organisation, with any organisation-wide mandatory policies | [optional] 
**reasoning_effort** | **str** | Override the reasoning effort. Must be one of the levels the effective model lists in capabilities.effortLevels. Omit or null to use the global agent value. | [optional] 
**version** | **int** | Current version for optimistic concurrency | [optional] 

## Example

```python
from quantcdn.models.upsert_agent_overlay_request import UpsertAgentOverlayRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpsertAgentOverlayRequest from a JSON string
upsert_agent_overlay_request_instance = UpsertAgentOverlayRequest.from_json(json)
# print the JSON string representation of the object
print(UpsertAgentOverlayRequest.to_json())

# convert the object into a dict
upsert_agent_overlay_request_dict = upsert_agent_overlay_request_instance.to_dict()
# create an instance of UpsertAgentOverlayRequest from a dict
upsert_agent_overlay_request_from_dict = UpsertAgentOverlayRequest.from_dict(upsert_agent_overlay_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


