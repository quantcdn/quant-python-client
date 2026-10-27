# V2KvUsage

Consumed read and write units per UTC day for the last 30 full days (ending yesterday), the table size and a list-price estimate (USD). Item count and size are updated by DynamoDB about every 6 hours. Never contains item values.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**store_name** | **str** |  | 
**format** | **int** |  | 
**state** | **str** |  | 
**table** | [**V2KvUsageTable**](V2KvUsageTable.md) |  | 
**retained_table** | [**V2KvUsageRetainedTable**](V2KvUsageRetainedTable.md) |  | [optional] 
**period** | [**V2KvUsagePeriod**](V2KvUsagePeriod.md) |  | 
**daily** | [**List[V2KvUsageDailyInner]**](V2KvUsageDailyInner.md) | Exactly period.days rows, oldest first. Units are rounded to 1 decimal. | 
**totals** | [**V2KvUsageTotals**](V2KvUsageTotals.md) |  | 
**estimate** | [**V2KvUsageEstimate**](V2KvUsageEstimate.md) |  | 

## Example

```python
from quantcdn.models.v2_kv_usage import V2KvUsage

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvUsage from a JSON string
v2_kv_usage_instance = V2KvUsage.from_json(json)
# print the JSON string representation of the object
print(V2KvUsage.to_json())

# convert the object into a dict
v2_kv_usage_dict = v2_kv_usage_instance.to_dict()
# create an instance of V2KvUsage from a dict
v2_kv_usage_from_dict = V2KvUsage.from_dict(v2_kv_usage_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


