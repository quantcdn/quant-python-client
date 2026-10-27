# V2KvUsageRetainedTable

Only while an upgrade keeps the format 1 table after the switch.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | 
**size_bytes** | **int** |  | 

## Example

```python
from quantcdn.models.v2_kv_usage_retained_table import V2KvUsageRetainedTable

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvUsageRetainedTable from a JSON string
v2_kv_usage_retained_table_instance = V2KvUsageRetainedTable.from_json(json)
# print the JSON string representation of the object
print(V2KvUsageRetainedTable.to_json())

# convert the object into a dict
v2_kv_usage_retained_table_dict = v2_kv_usage_retained_table_instance.to_dict()
# create an instance of V2KvUsageRetainedTable from a dict
v2_kv_usage_retained_table_from_dict = V2KvUsageRetainedTable.from_dict(v2_kv_usage_retained_table_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


