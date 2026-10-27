# GetSlackBotThread200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**content_trust** | **str** |  | [optional] 
**channel** | **str** |  | [optional] 
**thread_ts** | **str** |  | [optional] 
**permalink** | **str** |  | [optional] 
**messages** | [**List[AiSlackBotApiMessage]**](AiSlackBotApiMessage.md) |  | [optional] 
**code_job** | [**GetSlackBotThread200ResponseCodeJob**](GetSlackBotThread200ResponseCodeJob.md) |  | [optional] 
**next_cursor** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.get_slack_bot_thread200_response import GetSlackBotThread200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetSlackBotThread200Response from a JSON string
get_slack_bot_thread200_response_instance = GetSlackBotThread200Response.from_json(json)
# print the JSON string representation of the object
print(GetSlackBotThread200Response.to_json())

# convert the object into a dict
get_slack_bot_thread200_response_dict = get_slack_bot_thread200_response_instance.to_dict()
# create an instance of GetSlackBotThread200Response from a dict
get_slack_bot_thread200_response_from_dict = GetSlackBotThread200Response.from_dict(get_slack_bot_thread200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


