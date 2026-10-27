# AiSlackBotApiError


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | 
**error** | **bool** | Thin proxy for the Slack bot API: list API-enabled bots, read channel messages and threads, and post as the bot. The portal validates the request, requires a verified email, calls the platform and passes its status and body through. The platform owns the bot, channel and rate-limit rules and their error codes.  Only the values that SlackBotApiRequest returns go to the platform, never raw input. The activity entry (ai_slack_api) never holds message text. | 
**code** | **str** |  | 
**retryable** | **bool** |  | 
**slack_error** | **str** | The Slack error string. Only with code SLACK_ERROR. | [optional] 

## Example

```python
from quantcdn.models.ai_slack_bot_api_error import AiSlackBotApiError

# TODO update the JSON string below
json = "{}"
# create an instance of AiSlackBotApiError from a JSON string
ai_slack_bot_api_error_instance = AiSlackBotApiError.from_json(json)
# print the JSON string representation of the object
print(AiSlackBotApiError.to_json())

# convert the object into a dict
ai_slack_bot_api_error_dict = ai_slack_bot_api_error_instance.to_dict()
# create an instance of AiSlackBotApiError from a dict
ai_slack_bot_api_error_from_dict = AiSlackBotApiError.from_dict(ai_slack_bot_api_error_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


