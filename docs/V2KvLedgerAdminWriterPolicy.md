# V2KvLedgerAdminWriterPolicy

Immutable allowlist of internal Quant platform writers, included in definitionHash. With a writer policy, appends through the API are refused (only the listed platform services can write). Without it, appends work as usual. A ledger with personalFields must list quant-ledger, which writes the shred entries. This is not a read or management access policy.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform_principals** | **List[str]** | The platform service principals that may append (1 to 16, unique). | 

## Example

```python
from quantcdn.models.v2_kv_ledger_admin_writer_policy import V2KvLedgerAdminWriterPolicy

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvLedgerAdminWriterPolicy from a JSON string
v2_kv_ledger_admin_writer_policy_instance = V2KvLedgerAdminWriterPolicy.from_json(json)
# print the JSON string representation of the object
print(V2KvLedgerAdminWriterPolicy.to_json())

# convert the object into a dict
v2_kv_ledger_admin_writer_policy_dict = v2_kv_ledger_admin_writer_policy_instance.to_dict()
# create an instance of V2KvLedgerAdminWriterPolicy from a dict
v2_kv_ledger_admin_writer_policy_from_dict = V2KvLedgerAdminWriterPolicy.from_dict(v2_kv_ledger_admin_writer_policy_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


