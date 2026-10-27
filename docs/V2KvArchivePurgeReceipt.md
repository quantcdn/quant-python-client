# V2KvArchivePurgeReceipt

The platform's signed statement that the purge ran. It is not a proof of absence. json is the canonical (JCS) text that signature covers.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**var_json** | **str** | The canonical JSON text of the receipt. | 
**signature** | **str** | Base64 DER ECDSA signature over the SHA-256 of the json bytes. | 
**key_id** | **str** |  | 
**algorithm** | **str** |  | 

## Example

```python
from quantcdn.models.v2_kv_archive_purge_receipt import V2KvArchivePurgeReceipt

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvArchivePurgeReceipt from a JSON string
v2_kv_archive_purge_receipt_instance = V2KvArchivePurgeReceipt.from_json(json)
# print the JSON string representation of the object
print(V2KvArchivePurgeReceipt.to_json())

# convert the object into a dict
v2_kv_archive_purge_receipt_dict = v2_kv_archive_purge_receipt_instance.to_dict()
# create an instance of V2KvArchivePurgeReceipt from a dict
v2_kv_archive_purge_receipt_from_dict = V2KvArchivePurgeReceipt.from_dict(v2_kv_archive_purge_receipt_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


