# V1WafLogItem


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**timestamp** | **str** |  | 
**ip_address** | **str** |  | 
**location** | **str** |  | 
**asn** | **str** |  | 
**type** | **str** |  | 
**mode** | **str** |  | 
**rule_id** | **str** |  | 
**domain** | **str** |  | 
**url** | **str** |  | 
**method** | **str** |  | 
**user_agent** | **str** |  | 

## Example

```python
from quantcdn.models.v1_waf_log_item import V1WafLogItem

# TODO update the JSON string below
json = "{}"
# create an instance of V1WafLogItem from a JSON string
v1_waf_log_item_instance = V1WafLogItem.from_json(json)
# print the JSON string representation of the object
print(V1WafLogItem.to_json())

# convert the object into a dict
v1_waf_log_item_dict = v1_waf_log_item_instance.to_dict()
# create an instance of V1WafLogItem from a dict
v1_waf_log_item_from_dict = V1WafLogItem.from_dict(v1_waf_log_item_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


