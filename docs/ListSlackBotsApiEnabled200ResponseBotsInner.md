# ListSlackBotsApiEnabled200ResponseBotsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**bot_id** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**workspace_id** | **str** |  | [optional] 
**channels** | [**List[ListSlackBotsApiEnabled200ResponseBotsInnerChannelsInner]**](ListSlackBotsApiEnabled200ResponseBotsInnerChannelsInner.md) |  | [optional] 

## Example

```python
from quantcdn.models.list_slack_bots_api_enabled200_response_bots_inner import ListSlackBotsApiEnabled200ResponseBotsInner

# TODO update the JSON string below
json = "{}"
# create an instance of ListSlackBotsApiEnabled200ResponseBotsInner from a JSON string
list_slack_bots_api_enabled200_response_bots_inner_instance = ListSlackBotsApiEnabled200ResponseBotsInner.from_json(json)
# print the JSON string representation of the object
print(ListSlackBotsApiEnabled200ResponseBotsInner.to_json())

# convert the object into a dict
list_slack_bots_api_enabled200_response_bots_inner_dict = list_slack_bots_api_enabled200_response_bots_inner_instance.to_dict()
# create an instance of ListSlackBotsApiEnabled200ResponseBotsInner from a dict
list_slack_bots_api_enabled200_response_bots_inner_from_dict = ListSlackBotsApiEnabled200ResponseBotsInner.from_dict(list_slack_bots_api_enabled200_response_bots_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


