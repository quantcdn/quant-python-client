# V2KvLedgerProvenance

Who wrote the entry, set by the KV service from the authenticated caller (never from the body) and covered by the entry hash. platform: a Quant service (quant-ledger writes the shred entries); api: an API caller (an append through this API with a portal token records principal token:<token id>); dashboard: a portal user (principal: the portal user id); edge: an edge function (principal <org>/<project>/<function id>). An API caller with the API secret only records principal api-secret. Absent on entries written before provenance existed.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **str** |  | 
**principal** | **str** |  | 

## Example

```python
from quantcdn.models.v2_kv_ledger_provenance import V2KvLedgerProvenance

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvLedgerProvenance from a JSON string
v2_kv_ledger_provenance_instance = V2KvLedgerProvenance.from_json(json)
# print the JSON string representation of the object
print(V2KvLedgerProvenance.to_json())

# convert the object into a dict
v2_kv_ledger_provenance_dict = v2_kv_ledger_provenance_instance.to_dict()
# create an instance of V2KvLedgerProvenance from a dict
v2_kv_ledger_provenance_from_dict = V2KvLedgerProvenance.from_dict(v2_kv_ledger_provenance_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


