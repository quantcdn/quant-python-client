# ListSlackBotsApiEnabled200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**bots** | [**List[ListSlackBotsApiEnabled200ResponseBotsInner]**](ListSlackBotsApiEnabled200ResponseBotsInner.md) |  | [optional] 

## Example

```python
from quantcdn.models.list_slack_bots_api_enabled200_response import ListSlackBotsApiEnabled200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ListSlackBotsApiEnabled200Response from a JSON string
list_slack_bots_api_enabled200_response_instance = ListSlackBotsApiEnabled200Response.from_json(json)
# print the JSON string representation of the object
print(ListSlackBotsApiEnabled200Response.to_json())

# convert the object into a dict
list_slack_bots_api_enabled200_response_dict = list_slack_bots_api_enabled200_response_instance.to_dict()
# create an instance of ListSlackBotsApiEnabled200Response from a dict
list_slack_bots_api_enabled200_response_from_dict = ListSlackBotsApiEnabled200Response.from_dict(list_slack_bots_api_enabled200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


