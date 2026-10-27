# V2KvLedgerErasureShredReceiptDocument

The signed receipt with its parsed copy.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**var_json** | **str** | The RFC 8785 (JCS) text of the receipt that was signed. | 
**signature** | **str** | Base64 DER ECDSA P-256 signature over the SHA-256 of the UTF-8 bytes of json. | 
**key_id** | **str** | The KMS key ARN of the ledger key. | 
**algorithm** | **str** |  | 
**receipt** | [**V2KvLedgerErasureShredReceiptBody**](V2KvLedgerErasureShredReceiptBody.md) |  | 

## Example

```python
from quantcdn.models.v2_kv_ledger_erasure_shred_receipt_document import V2KvLedgerErasureShredReceiptDocument

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvLedgerErasureShredReceiptDocument from a JSON string
v2_kv_ledger_erasure_shred_receipt_document_instance = V2KvLedgerErasureShredReceiptDocument.from_json(json)
# print the JSON string representation of the object
print(V2KvLedgerErasureShredReceiptDocument.to_json())

# convert the object into a dict
v2_kv_ledger_erasure_shred_receipt_document_dict = v2_kv_ledger_erasure_shred_receipt_document_instance.to_dict()
# create an instance of V2KvLedgerErasureShredReceiptDocument from a dict
v2_kv_ledger_erasure_shred_receipt_document_from_dict = V2KvLedgerErasureShredReceiptDocument.from_dict(v2_kv_ledger_erasure_shred_receipt_document_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


