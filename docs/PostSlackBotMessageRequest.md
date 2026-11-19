# PostSlackBotMessageRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channel** | **str** |  | 
**thread_ts** | **str** | Absent: a root post | [optional] 
**text** | **str** | 1-8000 characters after trim | 
**format** | **str** | mrkdwn: Slack mrkdwn sections (default). markdown: standard Markdown in one Slack markdown block, including tables. | [optional] [default to 'mrkdwn']

## Example

```python
from quantcdn.models.post_slack_bot_message_request import PostSlackBotMessageRequest

# TODO update the JSON string below
json = "{}"
# create an instance of PostSlackBotMessageRequest from a JSON string
post_slack_bot_message_request_instance = PostSlackBotMessageRequest.from_json(json)
# print the JSON string representation of the object
print(PostSlackBotMessageRequest.to_json())

# convert the object into a dict
post_slack_bot_message_request_dict = post_slack_bot_message_request_instance.to_dict()
# create an instance of PostSlackBotMessageRequest from a dict
post_slack_bot_message_request_from_dict = PostSlackBotMessageRequest.from_dict(post_slack_bot_message_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


