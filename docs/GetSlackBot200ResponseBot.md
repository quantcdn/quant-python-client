# GetSlackBot200ResponseBot


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**bot_id** | **str** |  | [optional] 
**agent_id** | **str** |  | [optional] 
**setup_type** | **str** |  | [optional] 
**status** | **str** |  | [optional] 
**connected** | **bool** |  | [optional] 
**session_ttl_days** | **int** |  | [optional] 
**allowed_channels** | **List[str]** |  | [optional] 
**keywords_enabled** | **bool** |  | [optional] 
**keywords** | **List[str]** |  | [optional] 
**slash_commands** | **List[str]** |  | [optional] 
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


