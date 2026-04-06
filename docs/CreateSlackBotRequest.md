# CreateSlackBotRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**agent_id** | **str** | The AI agent that powers this bot | 
**setup_type** | **str** | Whether to use Quant-managed or customer-provided Slack app | 
**session_ttl_days** | **int** | Session TTL in days | [optional] 
**allowed_channels** | **List[str]** | Slack channel IDs the bot may respond in | [optional] 
**keywords_enabled** | **bool** | Whether keyword triggers are enabled | [optional] 
**keywords** | **List[str]** | Keywords that trigger the bot | [optional] 
**slash_commands** | **List[str]** | Slash commands the bot responds to | [optional] 

## Example

```python
from quantcdn.models.create_slack_bot_request import CreateSlackBotRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateSlackBotRequest from a JSON string
create_slack_bot_request_instance = CreateSlackBotRequest.from_json(json)
# print the JSON string representation of the object
print(CreateSlackBotRequest.to_json())

# convert the object into a dict
create_slack_bot_request_dict = create_slack_bot_request_instance.to_dict()
# create an instance of CreateSlackBotRequest from a dict
create_slack_bot_request_from_dict = CreateSlackBotRequest.from_dict(create_slack_bot_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


