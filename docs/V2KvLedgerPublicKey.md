# V2KvLedgerPublicKey

The public half of the KMS key that signs ledger digests, verification reports and shred receipts. Save publicKeyPem as key.pem for the offline verifier.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**key_id** | **str** | The KMS key ARN. | 
**algorithm** | **str** |  | 
**curve** | **str** |  | 
**public_key_pem** | **str** | SubjectPublicKeyInfo, PEM. | 
**keys** | [**List[V2KvLedgerPublicKeyKeysInner]**](V2KvLedgerPublicKeyKeysInner.md) | Current and historical verification keys. Select by the signature keyId. | [optional] 

## Example

```python
from quantcdn.models.v2_kv_ledger_public_key import V2KvLedgerPublicKey

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvLedgerPublicKey from a JSON string
v2_kv_ledger_public_key_instance = V2KvLedgerPublicKey.from_json(json)
# print the JSON string representation of the object
print(V2KvLedgerPublicKey.to_json())

# convert the object into a dict
v2_kv_ledger_public_key_dict = v2_kv_ledger_public_key_instance.to_dict()
# create an instance of V2KvLedgerPublicKey from a dict
v2_kv_ledger_public_key_from_dict = V2KvLedgerPublicKey.from_dict(v2_kv_ledger_public_key_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


