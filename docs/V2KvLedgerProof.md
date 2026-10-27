# V2KvLedgerProof

status pending: the entry is not archived and signed yet (about 10 minutes). status archived: the inclusion proof (RFC 9162 audit path). The body is the KV service bytes unchanged: digest is the signed RFC 8785 object.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | **str** |  | 
**entry** | [**V2KvLedgerProofEntry**](V2KvLedgerProofEntry.md) |  | [optional] 
**hash** | **str** |  | [optional] 
**source** | [**V2KvLedgerProvenance**](V2KvLedgerProvenance.md) |  | [optional] 
**period** | **str** | Archive period label, YYYYMMDDTHHmmZ. | [optional] 
**archive_key** | **str** |  | [optional] 
**leaf_index** | **int** |  | [optional] 
**tree_size** | **int** |  | [optional] 
**merkle_root** | **str** |  | [optional] 
**audit_path** | **List[str]** |  | [optional] 
**digest** | **Dict[str, object]** |  | [optional] 
**digest_key** | **str** |  | [optional] 
**signature** | **str** | Base64 DER ECDSA P-256 over SHA-256 of the digest bytes. | [optional] 
**key_id** | **str** |  | [optional] 
**digest_signed_at** | **datetime** |  | [optional] 
**anchor** | [**V2KvLedgerProofAnchor**](V2KvLedgerProofAnchor.md) |  | [optional] 
**anchor_unavailable** | **bool** |  | [optional] 

## Example

```python
from quantcdn.models.v2_kv_ledger_proof import V2KvLedgerProof

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvLedgerProof from a JSON string
v2_kv_ledger_proof_instance = V2KvLedgerProof.from_json(json)
# print the JSON string representation of the object
print(V2KvLedgerProof.to_json())

# convert the object into a dict
v2_kv_ledger_proof_dict = v2_kv_ledger_proof_instance.to_dict()
# create an instance of V2KvLedgerProof from a dict
v2_kv_ledger_proof_from_dict = V2KvLedgerProof.from_dict(v2_kv_ledger_proof_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


