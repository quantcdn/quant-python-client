# GetSlackBot200ResponseBot


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
**allowed_channels** | **List[str]** |  | [optional] 
**allowed_users** | **List[str]** |  | [optional] 
**denied_users** | **List[str]** |  | [optional] 
**allow_guests** | **bool** |  | [optional] 
**home_tab_content** | **str** |  | [optional] 
**agent_access_control** | **object** |  | [optional] 
**keywords_enabled** | **bool** |  | [optional] 
**keywords** | **List[str]** |  | [optional] 
**created_at** | **datetime** |  | [optional] 
**updated_at** | **datetime** |  | [optional] 

## Example

```python
from quantcdn.models.get_slack_bot200_response_bot import GetSlackBot200ResponseBot

# TODO update the JSON string below
json = "{}"
# create an instance of GetSlackBot200ResponseBot from a JSON string
get_slack_bot200_response_bot_instance = GetSlackBot200ResponseBot.from_json(json)
# print the JSON string representation of the object
print(GetSlackBot200ResponseBot.to_json())

# convert the object into a dict
get_slack_bot200_response_bot_dict = get_slack_bot200_response_bot_instance.to_dict()
# create an instance of GetSlackBot200ResponseBot from a dict
get_slack_bot200_response_bot_from_dict = GetSlackBot200ResponseBot.from_dict(get_slack_bot200_response_bot_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


