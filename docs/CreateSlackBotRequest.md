# CreateSlackBotRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | Display name for the bot | 
**setup_type** | **str** | Whether to use Quant-managed or customer-provided Slack app | 
**system_prompt** | **str** | System prompt for the backing AI agent | 
**model_id** | **str** | AI model identifier | 
**temperature** | **float** | Sampling temperature | [optional] 
**max_tokens** | **int** | Maximum response tokens | [optional] 
**allowed_tools** | **List[str]** | Tools the agent may use | [optional] 
**assigned_skills** | **List[str]** | Skills assigned to the agent | [optional] 
**allowed_collections** | **List[str]** | Vector DB collections the agent may query | [optional] 
**allowed_sub_agents** | **List[str]** | Sub-agents the agent may call | [optional] 
**guardrail_preset** | **str** | Guardrail preset name | [optional] 
**filter_policies** | **List[str]** | Content filter policies | [optional] 
**long_context** | **bool** | Enable long context mode | [optional] 
**session_ttl_days** | **int** | Session TTL in days | [optional] 
**allowed_channels** | **List[str]** | Slack channel IDs the bot may respond in | [optional] 
**allowed_users** | **List[str]** | Slack user IDs allowed to interact with the bot | [optional] 
**denied_users** | **List[str]** | Slack user IDs denied from interacting with the bot | [optional] 
**allow_guests** | **bool** | Whether guest users may interact with the bot | [optional] 
**home_tab_content** | **str** | Content shown on the bot&#39;s Home tab in Slack | [optional] 
**agent_access_control** | **object** | Agent-level access control settings | [optional] 
**keywords_enabled** | **bool** | Whether keyword triggers are enabled | [optional] 
**keywords** | **List[str]** | Keywords that trigger the bot | [optional] 

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


