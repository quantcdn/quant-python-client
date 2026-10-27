# V2KvLedgerArchive

One page of presigned download URLs (each valid for up to 3600 seconds; call again for fresh URLs). Every key is under this store's prefixes ledgers/<org>/<store>/<ledger>/ and digests/<org>/<store>/.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**objects** | [**List[V2KvLedgerArchiveObject]**](V2KvLedgerArchiveObject.md) |  | 
**digests** | [**List[V2KvLedgerArchiveDigest]**](V2KvLedgerArchiveDigest.md) | First page (or digest_cursor pages) only. | 
**timestamps** | [**List[V2KvLedgerArchiveFile]**](V2KvLedgerArchiveFile.md) | RFC 3161 tokens and anchor binding files. First page (or digest_cursor pages) only. | 
**digests_truncated** | **bool** | True when more than 2,000 digest files exist: continue with next_digest_cursor. | [optional] 
**note** | **str** |  | [optional] 
**next_cursor** | **str** | Pass as cursor for the next page of objects. | 
**next_digest_cursor** | **str** | Pass as digest_cursor for the next page of digests. | 

## Example

```python
from quantcdn.models.v2_kv_ledger_archive import V2KvLedgerArchive

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvLedgerArchive from a JSON string
v2_kv_ledger_archive_instance = V2KvLedgerArchive.from_json(json)
# print the JSON string representation of the object
print(V2KvLedgerArchive.to_json())

# convert the object into a dict
v2_kv_ledger_archive_dict = v2_kv_ledger_archive_instance.to_dict()
# create an instance of V2KvLedgerArchive from a dict
v2_kv_ledger_archive_from_dict = V2KvLedgerArchive.from_dict(v2_kv_ledger_archive_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


