# PostSlackBotFile201Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channel** | **str** |  | [optional] 
**thread_ts** | **str** |  | [optional] 
**file_id** | **str** |  | [optional] 
**permalink** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.post_slack_bot_file201_response import PostSlackBotFile201Response

# TODO update the JSON string below
json = "{}"
# create an instance of PostSlackBotFile201Response from a JSON string
post_slack_bot_file201_response_instance = PostSlackBotFile201Response.from_json(json)
# print the JSON string representation of the object
print(PostSlackBotFile201Response.to_json())

# convert the object into a dict
post_slack_bot_file201_response_dict = post_slack_bot_file201_response_instance.to_dict()
# create an instance of PostSlackBotFile201Response from a dict
post_slack_bot_file201_response_from_dict = PostSlackBotFile201Response.from_dict(post_slack_bot_file201_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


