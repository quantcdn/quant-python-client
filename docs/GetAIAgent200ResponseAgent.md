# GetAIAgent200ResponseAgent


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**agent_id** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**group** | **str** |  | [optional] 
**system_prompt** | **str** |  | [optional] 
**model_id** | **str** |  | [optional] 
**temperature** | **float** |  | [optional] 
**max_tokens** | **int** |  | [optional] 
**allowed_tools** | **List[str]** |  | [optional] 
**allowed_collections** | **List[str]** |  | [optional] 
**created_by** | **str** |  | [optional] 
**created_at** | **datetime** |  | [optional] 
**updated_at** | **datetime** |  | [optional] 

## Example

```python
from quantcdn.models.get_ai_agent200_response_agent import GetAIAgent200ResponseAgent

# TODO update the JSON string below
json = "{}"
# create an instance of GetAIAgent200ResponseAgent from a JSON string
get_ai_agent200_response_agent_instance = GetAIAgent200ResponseAgent.from_json(json)
# print the JSON string representation of the object
print(GetAIAgent200ResponseAgent.to_json())

# convert the object into a dict
get_ai_agent200_response_agent_dict = get_ai_agent200_response_agent_instance.to_dict()
# create an instance of GetAIAgent200ResponseAgent from a dict
get_ai_agent200_response_agent_from_dict = GetAIAgent200ResponseAgent.from_dict(get_ai_agent200_response_agent_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


