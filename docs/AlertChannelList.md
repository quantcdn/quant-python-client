# AlertChannelList


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channels** | [**List[AlertChannelSummary]**](AlertChannelSummary.md) |  | 

## Example

```python
from quantcdn.models.alert_channel_list import AlertChannelList

# TODO update the JSON string below
json = "{}"
# create an instance of AlertChannelList from a JSON string
alert_channel_list_instance = AlertChannelList.from_json(json)
# print the JSON string representation of the object
print(AlertChannelList.to_json())

# convert the object into a dict
alert_channel_list_dict = alert_channel_list_instance.to_dict()
# create an instance of AlertChannelList from a dict
alert_channel_list_from_dict = AlertChannelList.from_dict(alert_channel_list_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


