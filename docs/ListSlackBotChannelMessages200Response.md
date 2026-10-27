# ListSlackBotChannelMessages200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**content_trust** | **str** |  | [optional] 
**channel** | **str** |  | [optional] 
**messages** | [**List[AiSlackBotApiMessage]**](AiSlackBotApiMessage.md) |  | [optional] 
**next_cursor** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.list_slack_bot_channel_messages200_response import ListSlackBotChannelMessages200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ListSlackBotChannelMessages200Response from a JSON string
list_slack_bot_channel_messages200_response_instance = ListSlackBotChannelMessages200Response.from_json(json)
# print the JSON string representation of the object
print(ListSlackBotChannelMessages200Response.to_json())

# convert the object into a dict
list_slack_bot_channel_messages200_response_dict = list_slack_bot_channel_messages200_response_instance.to_dict()
# create an instance of ListSlackBotChannelMessages200Response from a dict
list_slack_bot_channel_messages200_response_from_dict = ListSlackBotChannelMessages200Response.from_dict(list_slack_bot_channel_messages200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


