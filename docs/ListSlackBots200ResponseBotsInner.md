# ListSlackBots200ResponseBotsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**bot_id** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**setup_type** | **str** |  | [optional] 
**status** | **str** |  | [optional] 
**connected** | **bool** |  | [optional] 
**system_prompt** | **str** |  | [optional] 
**model_id** | **str** |  | [optional] 
**temperature** | **float** |  | [optional] 
**max_tokens** | **int** |  | [optional] 
**allowed_tools** | **List[str]** |  | [optional] 
**assigned_skills** | **List[str]** |  | [optional] 
**allowed_collections** | **List[str]** |  | [optional] 
**allowed_sub_agents** | **List[str]** |  | [optional] 
**guardrail_preset** | **str** |  | [optional] 
**filter_policies** | **List[str]** |  | [optional] 
**long_context** | **bool** |  | [optional] 
**session_ttl_days** | **int** |  | [optional] 
**keywords_enabled** | **bool** |  | [optional] 
**created_at** | **datetime** |  | [optional] 

## Example

```python
from quantcdn.models.list_slack_bots200_response_bots_inner import ListSlackBots200ResponseBotsInner

# TODO update the JSON string below
json = "{}"
# create an instance of ListSlackBots200ResponseBotsInner from a JSON string
list_slack_bots200_response_bots_inner_instance = ListSlackBots200ResponseBotsInner.from_json(json)
# print the JSON string representation of the object
print(ListSlackBots200ResponseBotsInner.to_json())

# convert the object into a dict
list_slack_bots200_response_bots_inner_dict = list_slack_bots200_response_bots_inner_instance.to_dict()
# create an instance of ListSlackBots200ResponseBotsInner from a dict
list_slack_bots200_response_bots_inner_from_dict = ListSlackBots200ResponseBotsInner.from_dict(list_slack_bots200_response_bots_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


