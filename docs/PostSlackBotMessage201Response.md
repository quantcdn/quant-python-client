# PostSlackBotMessage201Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channel** | **str** |  | [optional] 
**ts** | **str** |  | [optional] 
**thread_ts** | **str** |  | [optional] 
**permalink** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.post_slack_bot_message201_response import PostSlackBotMessage201Response

# TODO update the JSON string below
json = "{}"
# create an instance of PostSlackBotMessage201Response from a JSON string
post_slack_bot_message201_response_instance = PostSlackBotMessage201Response.from_json(json)
# print the JSON string representation of the object
print(PostSlackBotMessage201Response.to_json())

# convert the object into a dict
post_slack_bot_message201_response_dict = post_slack_bot_message201_response_instance.to_dict()
# create an instance of PostSlackBotMessage201Response from a dict
post_slack_bot_message201_response_from_dict = PostSlackBotMessage201Response.from_dict(post_slack_bot_message201_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


