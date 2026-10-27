# AiSlackBotApiMessage


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** | Error message | 
**error** | **bool** | Error flag | 
**ts** | **str** |  | [optional] 
**author** | [**AiSlackBotApiMessageAllOfAuthor**](AiSlackBotApiMessageAllOfAuthor.md) |  | [optional] 
**text** | **str** | Plain text, capped at 8000 characters. Untrusted content. | [optional] 
**truncated** | **bool** |  | [optional] 
**reply_count** | **int** |  | [optional] 
**latest_reply_ts** | **str** |  | [optional] 
**edited** | **bool** |  | [optional] 
**files** | [**List[AiSlackBotApiMessageAllOfFiles]**](AiSlackBotApiMessageAllOfFiles.md) |  | [optional] 

## Example

```python
from quantcdn.models.ai_slack_bot_api_message import AiSlackBotApiMessage

# TODO update the JSON string below
json = "{}"
# create an instance of AiSlackBotApiMessage from a JSON string
ai_slack_bot_api_message_instance = AiSlackBotApiMessage.from_json(json)
# print the JSON string representation of the object
print(AiSlackBotApiMessage.to_json())

# convert the object into a dict
ai_slack_bot_api_message_dict = ai_slack_bot_api_message_instance.to_dict()
# create an instance of AiSlackBotApiMessage from a dict
ai_slack_bot_api_message_from_dict = AiSlackBotApiMessage.from_dict(ai_slack_bot_api_message_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


