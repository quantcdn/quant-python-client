# V2KvLedgerArchiveDigest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**key** | **str** | digests/&lt;org&gt;/&lt;store&gt;/&lt;period&gt;.json (a supplementary digest is &lt;period&gt;_&lt;n&gt;.json). | 
**url** | **str** |  | 
**sig_url** | **str** | Presigned URL of &lt;key&gt;.sig; absent if the signature does not exist yet. | [optional] 
**period** | **str** |  | 
**name** | **str** |  | 

## Example

```python
from quantcdn.models.v2_kv_ledger_archive_digest import V2KvLedgerArchiveDigest

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvLedgerArchiveDigest from a JSON string
v2_kv_ledger_archive_digest_instance = V2KvLedgerArchiveDigest.from_json(json)
# print the JSON string representation of the object
print(V2KvLedgerArchiveDigest.to_json())

# convert the object into a dict
v2_kv_ledger_archive_digest_dict = v2_kv_ledger_archive_digest_instance.to_dict()
# create an instance of V2KvLedgerArchiveDigest from a dict
v2_kv_ledger_archive_digest_from_dict = V2KvLedgerArchiveDigest.from_dict(v2_kv_ledger_archive_digest_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


