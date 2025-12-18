# WafConfigThresholdsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **str** | Threshold type | [optional] 
**rps** | **int** | Requests per second limit (for ip/header) | [optional] 
**hits** | **int** | Hit count limit (for waf_hit_by_ip) | [optional] 
**minutes** | **int** | Time window in minutes (for waf_hit_by_ip) | [optional] 
**cooldown** | **int** | Cooldown period in seconds | [optional] 
**mode** | **str** | Threshold enforcement mode | [optional] [default to 'disabled']
**value** | **str** | Header name (for header type) | [optional] 
**notify_slack** | **str** | Slack webhook for this threshold | [optional] 

## Example

```python
from quantcdn.models.waf_config_thresholds_inner import WafConfigThresholdsInner

# TODO update the JSON string below
json = "{}"
# create an instance of WafConfigThresholdsInner from a JSON string
waf_config_thresholds_inner_instance = WafConfigThresholdsInner.from_json(json)
# print the JSON string representation of the object
print(WafConfigThresholdsInner.to_json())

# convert the object into a dict
waf_config_thresholds_inner_dict = waf_config_thresholds_inner_instance.to_dict()
# create an instance of WafConfigThresholdsInner from a dict
waf_config_thresholds_inner_from_dict = WafConfigThresholdsInner.from_dict(waf_config_thresholds_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


