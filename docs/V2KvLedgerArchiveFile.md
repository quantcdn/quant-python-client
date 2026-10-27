# V2KvLedgerArchiveFile


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**key** | **str** | digests/&lt;org&gt;/&lt;store&gt;/anchors/&lt;YYYYMMDD&gt;.tsr or .anchor.json. | 
**url** | **str** |  | 

## Example

```python
from quantcdn.models.v2_kv_ledger_archive_file import V2KvLedgerArchiveFile

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvLedgerArchiveFile from a JSON string
v2_kv_ledger_archive_file_instance = V2KvLedgerArchiveFile.from_json(json)
# print the JSON string representation of the object
print(V2KvLedgerArchiveFile.to_json())

# convert the object into a dict
v2_kv_ledger_archive_file_dict = v2_kv_ledger_archive_file_instance.to_dict()
# create an instance of V2KvLedgerArchiveFile from a dict
v2_kv_ledger_archive_file_from_dict = V2KvLedgerArchiveFile.from_dict(v2_kv_ledger_archive_file_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


