# V2KvUsageTable


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | 
**item_count** | **int** |  | 
**size_bytes** | **int** | Table data only. | 
**index_size_bytes** | **int** | Sum of the secondary index sizes (0 when none). | 

## Example

```python
from quantcdn.models.v2_kv_usage_table import V2KvUsageTable

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvUsageTable from a JSON string
v2_kv_usage_table_instance = V2KvUsageTable.from_json(json)
# print the JSON string representation of the object
print(V2KvUsageTable.to_json())

# convert the object into a dict
v2_kv_usage_table_dict = v2_kv_usage_table_instance.to_dict()
# create an instance of V2KvUsageTable from a dict
v2_kv_usage_table_from_dict = V2KvUsageTable.from_dict(v2_kv_usage_table_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


