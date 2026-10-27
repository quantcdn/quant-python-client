# V2KvUsageEstimatePrices


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**read_per_million** | **float** |  | 
**write_per_million** | **float** |  | 
**storage_per_gb_month** | **float** |  | 
**pitr_per_gb_month** | **float** |  | 

## Example

```python
from quantcdn.models.v2_kv_usage_estimate_prices import V2KvUsageEstimatePrices

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvUsageEstimatePrices from a JSON string
v2_kv_usage_estimate_prices_instance = V2KvUsageEstimatePrices.from_json(json)
# print the JSON string representation of the object
print(V2KvUsageEstimatePrices.to_json())

# convert the object into a dict
v2_kv_usage_estimate_prices_dict = v2_kv_usage_estimate_prices_instance.to_dict()
# create an instance of V2KvUsageEstimatePrices from a dict
v2_kv_usage_estimate_prices_from_dict = V2KvUsageEstimatePrices.from_dict(v2_kv_usage_estimate_prices_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


