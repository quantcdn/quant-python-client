# UpdateSlackBotRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**agent_id** | **str** | Change the backing AI agent | [optional] 
**status** | **str** | Enable or disable the bot | [optional] 
**session_ttl_days** | **int** | Session TTL in days | [optional] 
**allowed_channels** | **List[str]** | Slack channel IDs the bot may respond in | [optional] 
**keywords_enabled** | **bool** | Whether keyword triggers are enabled | [optional] 
**keywords** | **List[str]** | Keywords that trigger the bot | [optional] 
**slash_commands** | **List[str]** | Slash commands the bot responds to | [optional] 

## Example

```python
from quantcdn.models.update_slack_bot_request import UpdateSlackBotRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateSlackBotRequest from a JSON string
update_slack_bot_request_instance = UpdateSlackBotRequest.from_json(json)
# print the JSON string representation of the object
print(UpdateSlackBotRequest.to_json())

# convert the object into a dict
update_slack_bot_request_dict = update_slack_bot_request_instance.to_dict()
# create an instance of UpdateSlackBotRequest from a dict
update_slack_bot_request_from_dict = UpdateSlackBotRequest.from_dict(update_slack_bot_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


