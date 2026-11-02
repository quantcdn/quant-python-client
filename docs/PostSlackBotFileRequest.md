# PostSlackBotFileRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channel** | **str** |  | 
**thread_ts** | **str** | Absent: a root post | [optional] 
**content** | **str** | The image, base64 (standard alphabet, no whitespace, no data: prefix). 1 byte to 4 MiB decoded. | 
**filename** | **str** | Default screenshot.&lt;ext&gt;. The extension must match the image type (png, jpg, jpeg, gif, webp). | [optional] 
**title** | **str** |  | [optional] 
**alt_text** | **str** |  | [optional] 
**text** | **str** | Caption. Same mention rules as a message. | [optional] 

## Example

```python
from quantcdn.models.post_slack_bot_file_request import PostSlackBotFileRequest

# TODO update the JSON string below
json = "{}"
# create an instance of PostSlackBotFileRequest from a JSON string
post_slack_bot_file_request_instance = PostSlackBotFileRequest.from_json(json)
# print the JSON string representation of the object
print(PostSlackBotFileRequest.to_json())

# convert the object into a dict
post_slack_bot_file_request_dict = post_slack_bot_file_request_instance.to_dict()
# create an instance of PostSlackBotFileRequest from a dict
post_slack_bot_file_request_from_dict = PostSlackBotFileRequest.from_dict(post_slack_bot_file_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


