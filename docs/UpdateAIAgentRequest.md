# UpdateAIAgentRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**group** | **str** |  | [optional] 
**system_prompt** | **str** |  | [optional] 
**temperature** | **float** |  | [optional] 
**model_id** | **str** |  | [optional] 
**max_tokens** | **int** |  | [optional] 
**allowed_tools** | **List[str]** |  | [optional] 
**allowed_collections** | **List[str]** |  | [optional] 

## Example

```python
from quantcdn.models.update_ai_agent_request import UpdateAIAgentRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateAIAgentRequest from a JSON string
update_ai_agent_request_instance = UpdateAIAgentRequest.from_json(json)
# print the JSON string representation of the object
print(UpdateAIAgentRequest.to_json())

# convert the object into a dict
update_ai_agent_request_dict = update_ai_agent_request_instance.to_dict()
# create an instance of UpdateAIAgentRequest from a dict
update_ai_agent_request_from_dict = UpdateAIAgentRequest.from_dict(update_ai_agent_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


