# CreateAIAgentRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | 
**description** | **str** |  | 
**group** | **str** |  | [optional] 
**system_prompt** | **str** |  | 
**temperature** | **float** |  | [optional] 
**model_id** | **str** |  | 
**max_tokens** | **int** |  | [optional] 
**allowed_tools** | **List[str]** |  | [optional] 
**allowed_collections** | **List[str]** |  | [optional] 
**assigned_skills** | **List[str]** | Skill IDs to assign to this agent | [optional] 
**created_by** | **str** | User identifier who created the agent | [optional] 
**long_context** | **bool** | Enable 1M context window support | [optional] 
**guardrail_preset** | **str** | Guardrail preset name | [optional] 
**filter_policies** | **List[str]** | Filter policy IDs to apply to this agent&#39;s inference requests | [optional] 

## Example

```python
from quantcdn.models.create_ai_agent_request import CreateAIAgentRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateAIAgentRequest from a JSON string
create_ai_agent_request_instance = CreateAIAgentRequest.from_json(json)
# print the JSON string representation of the object
print(CreateAIAgentRequest.to_json())

# convert the object into a dict
create_ai_agent_request_dict = create_ai_agent_request_instance.to_dict()
# create an instance of CreateAIAgentRequest from a dict
create_ai_agent_request_from_dict = CreateAIAgentRequest.from_dict(create_ai_agent_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


