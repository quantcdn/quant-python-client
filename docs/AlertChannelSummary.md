# AlertChannelSummary

An alert channel as the public API returns it. The secret (webhook URL or address list) is never returned.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | The channel ID | 
**name** | **str** |  | 
**type** | **str** |  | 
**hint** | **str** | A masked hint of the destination | 

## Example

```python
from quantcdn.models.alert_channel_summary import AlertChannelSummary

# TODO update the JSON string below
json = "{}"
# create an instance of AlertChannelSummary from a JSON string
alert_channel_summary_instance = AlertChannelSummary.from_json(json)
# print the JSON string representation of the object
print(AlertChannelSummary.to_json())

# convert the object into a dict
alert_channel_summary_dict = alert_channel_summary_instance.to_dict()
# create an instance of AlertChannelSummary from a dict
alert_channel_summary_from_dict = AlertChannelSummary.from_dict(alert_channel_summary_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


