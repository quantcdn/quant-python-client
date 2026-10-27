# V2KvIndex

A declared index. States: BUILDING (declared; writes maintain it after about 40 seconds and the backfill runs after about 75 seconds; lookup and count answer 409 INDEX_NOT_READY), ACTIVE (built; lookup, count and index list queries work), FAILED (the build stopped; see error and conflicts; drop and declare again), DROPPING (a drop is in progress; the index then disappears and KV_indexes_show answers 404 INDEX_NOT_FOUND). Terraform and other clients wait for ACTIVE by polling KV_indexes_show; FAILED is terminal.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | 
**collection** | **str** |  | 
**fields** | **List[str]** |  | 
**sort_by** | **str** |  | [optional] 
**unique** | **bool** |  | [optional] 
**count** | **bool** |  | [optional] 
**slot** | **int** | The secondary index slot that serves the index. | 
**state** | **str** |  | 
**created_at** | **datetime** |  | 
**error** | **str** | FAILED only: the code of the first problem the build found. | [optional] 
**conflicts** | **List[str]** | FAILED only: up to 20 keys (16 KiB) that caused the failure, without duplicates. | [optional] 
**job** | [**V2KvIndexJob**](V2KvIndexJob.md) |  | [optional] 

## Example

```python
from quantcdn.models.v2_kv_index import V2KvIndex

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvIndex from a JSON string
v2_kv_index_instance = V2KvIndex.from_json(json)
# print the JSON string representation of the object
print(V2KvIndex.to_json())

# convert the object into a dict
v2_kv_index_dict = v2_kv_index_instance.to_dict()
# create an instance of V2KvIndex from a dict
v2_kv_index_from_dict = V2KvIndex.from_dict(v2_kv_index_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


