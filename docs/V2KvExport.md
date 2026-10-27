# V2KvExport

An export of the whole store to gzip JSON Lines files (key, value, createdAt, updatedAt and, when present, expiresAt, version, encrypted). Secret values are exported as [ENCRYPTED]; ledger personal fields as [PERSONAL] (the row adds personal). Expired items are left out. Files are kept until expiresAt (7 days).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | ULID of the export. | 
**phase** | **str** |  | 
**requested_at** | **datetime** |  | 
**updated_at** | **datetime** | Moves on every step. An export in progress whose updatedAt is older than 960 seconds can be resumed. | 
**export_time** | **datetime** | The point in time the export reads. | [optional] 
**completed_at** | **datetime** |  | [optional] 
**item_count** | **int** |  | [optional] 
**skipped** | [**V2KvExportSkipped**](V2KvExportSkipped.md) |  | [optional] 
**size_bytes** | **int** | Total size of the compressed files. | [optional] 
**parts** | **int** |  | [optional] 
**expires_at** | **datetime** |  | [optional] 
**error** | **str** |  | [optional] 
**downloads** | [**List[V2KvExportDownload]**](V2KvExportDownload.md) | Phase done only. | [optional] 

## Example

```python
from quantcdn.models.v2_kv_export import V2KvExport

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvExport from a JSON string
v2_kv_export_instance = V2KvExport.from_json(json)
# print the JSON string representation of the object
print(V2KvExport.to_json())

# convert the object into a dict
v2_kv_export_dict = v2_kv_export_instance.to_dict()
# create an instance of V2KvExport from a dict
v2_kv_export_from_dict = V2KvExport.from_dict(v2_kv_export_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


