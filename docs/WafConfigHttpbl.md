# WafConfigHttpbl

Project Honey Pot HTTP:BL configuration

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**httpbl_enabled** | **bool** | Enable HTTP:BL | [optional] [default to False]
**block_suspicious** | **bool** | Block suspicious IPs | [optional] [default to False]
**block_harvester** | **bool** | Block email harvesters | [optional] [default to False]
**block_spam** | **bool** | Block spam sources | [optional] [default to False]
**block_search_engine** | **bool** | Block search engines | [optional] [default to False]
**httpbl_key** | **str** | HTTP:BL API key | [optional] 

## Example

```python
from quantcdn.models.waf_config_httpbl import WafConfigHttpbl

# TODO update the JSON string below
json = "{}"
# create an instance of WafConfigHttpbl from a JSON string
waf_config_httpbl_instance = WafConfigHttpbl.from_json(json)
# print the JSON string representation of the object
print(WafConfigHttpbl.to_json())

# convert the object into a dict
waf_config_httpbl_dict = waf_config_httpbl_instance.to_dict()
# create an instance of WafConfigHttpbl from a dict
waf_config_httpbl_from_dict = WafConfigHttpbl.from_dict(waf_config_httpbl_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


