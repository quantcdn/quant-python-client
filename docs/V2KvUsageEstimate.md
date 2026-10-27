# V2KvUsageEstimate

List-price estimate (USD, 4 decimals). Excludes the free tier, the request Lambda and data transfer.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**currency** | **str** |  | 
**read_cost** | **float** |  | 
**write_cost** | **float** |  | 
**request_cost30_days** | **float** | readCost + writeCost. | 
**storage_cost_per_month** | **float** |  | 
**pitr_cost_per_month** | **float** |  | 
**prices** | [**V2KvUsageEstimatePrices**](V2KvUsageEstimatePrices.md) |  | 
**note** | **str** |  | 

## Example

```python
from quantcdn.models.v2_kv_usage_estimate import V2KvUsageEstimate

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvUsageEstimate from a JSON string
v2_kv_usage_estimate_instance = V2KvUsageEstimate.from_json(json)
# print the JSON string representation of the object
print(V2KvUsageEstimate.to_json())

# convert the object into a dict
v2_kv_usage_estimate_dict = v2_kv_usage_estimate_instance.to_dict()
# create an instance of V2KvUsageEstimate from a dict
v2_kv_usage_estimate_from_dict = V2KvUsageEstimate.from_dict(v2_kv_usage_estimate_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


