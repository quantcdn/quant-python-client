# V2KvLedgerArchiveObject


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**key** | **str** | ledgers/&lt;org&gt;/&lt;store&gt;/&lt;ledger&gt;/&lt;collection base64url&gt;/&lt;shard&gt;/&lt;period&gt;-&lt;fromSeq 12&gt;-&lt;toSeq 12&gt;.jsonl.gz. Save the file under this path. | 
**url** | **str** | Presigned GET URL, valid for up to 3600 seconds. | 
**collection** | **str** |  | 
**shard** | **str** |  | 
**from_seq** | **int** |  | 
**to_seq** | **int** |  | 
**period** | **str** |  | 

## Example

```python
from quantcdn.models.v2_kv_ledger_archive_object import V2KvLedgerArchiveObject

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvLedgerArchiveObject from a JSON string
v2_kv_ledger_archive_object_instance = V2KvLedgerArchiveObject.from_json(json)
# print the JSON string representation of the object
print(V2KvLedgerArchiveObject.to_json())

# convert the object into a dict
v2_kv_ledger_archive_object_dict = v2_kv_ledger_archive_object_instance.to_dict()
# create an instance of V2KvLedgerArchiveObject from a dict
v2_kv_ledger_archive_object_from_dict = V2KvLedgerArchiveObject.from_dict(v2_kv_ledger_archive_object_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


