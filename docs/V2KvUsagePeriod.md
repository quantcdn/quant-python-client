# V2KvUsagePeriod


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**start** | **date** |  | 
**end** | **date** | Yesterday (UTC). | 
**days** | **int** |  | 

## Example

```python
from quantcdn.models.v2_kv_usage_period import V2KvUsagePeriod

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvUsagePeriod from a JSON string
v2_kv_usage_period_instance = V2KvUsagePeriod.from_json(json)
# print the JSON string representation of the object
print(V2KvUsagePeriod.to_json())

# convert the object into a dict
v2_kv_usage_period_dict = v2_kv_usage_period_instance.to_dict()
# create an instance of V2KvUsagePeriod from a dict
v2_kv_usage_period_from_dict = V2KvUsagePeriod.from_dict(v2_kv_usage_period_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


