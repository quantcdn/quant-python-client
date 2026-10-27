# V2KvLedgerErasureSignedShredReceipt

The signed receipt of an erasure. Save the object as a file to check it with kv-ledger-verify verify-signed. Only json is signed: parse it, do not re-serialise it.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**var_json** | **str** | The RFC 8785 (JCS) text of the receipt that was signed. | 
**signature** | **str** | Base64 DER ECDSA P-256 signature over the SHA-256 of the UTF-8 bytes of json. | 
**key_id** | **str** | The KMS key ARN of the ledger key. | 
**algorithm** | **str** |  | 

## Example

```python
from quantcdn.models.v2_kv_ledger_erasure_signed_shred_receipt import V2KvLedgerErasureSignedShredReceipt

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvLedgerErasureSignedShredReceipt from a JSON string
v2_kv_ledger_erasure_signed_shred_receipt_instance = V2KvLedgerErasureSignedShredReceipt.from_json(json)
# print the JSON string representation of the object
print(V2KvLedgerErasureSignedShredReceipt.to_json())

# convert the object into a dict
v2_kv_ledger_erasure_signed_shred_receipt_dict = v2_kv_ledger_erasure_signed_shred_receipt_instance.to_dict()
# create an instance of V2KvLedgerErasureSignedShredReceipt from a dict
v2_kv_ledger_erasure_signed_shred_receipt_from_dict = V2KvLedgerErasureSignedShredReceipt.from_dict(v2_kv_ledger_erasure_signed_shred_receipt_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


