# WafConfigBlockLists

Enable predefined block lists

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**user_agent** | **bool** | Block known bad user agents | [optional] [default to False]
**referer** | **bool** | Block known bad referers | [optional] [default to False]
**ip** | **bool** | Block known bad IPs | [optional] [default to False]
**ai** | **bool** | Block AI crawlers | [optional] [default to False]

## Example

```python
from quantcdn.models.waf_config_block_lists import WafConfigBlockLists

# TODO update the JSON string below
json = "{}"
# create an instance of WafConfigBlockLists from a JSON string
waf_config_block_lists_instance = WafConfigBlockLists.from_json(json)
# print the JSON string representation of the object
print(WafConfigBlockLists.to_json())

# convert the object into a dict
waf_config_block_lists_dict = waf_config_block_lists_instance.to_dict()
# create an instance of WafConfigBlockLists from a dict
waf_config_block_lists_from_dict = WafConfigBlockLists.from_dict(waf_config_block_lists_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


