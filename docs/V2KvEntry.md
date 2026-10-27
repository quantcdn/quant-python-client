# V2KvEntry

One key with its metadata. A ledger entry adds ledger and has no version. On a ledger entry, personal fields read \"[PERSONAL]\" and personal names them, unless the caller revealed them (reveal=true with the ledger_reveal permission). Unless revealed, the subject field of a pseudonym ledger shows the subject token (or \"[PERSONAL]\", listed in personal). A shredded personal field reads {\"$shredded\": true}.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**key** | **str** |  | 
**value** | **object** | The stored JSON value (any JSON type), decrypted when it was stored as a secret. In a key list a secret value reads [ENCRYPTED]. | [optional] 
**encrypted** | **bool** | True when the value was stored as a secret. | [optional] 
**status** | **str** | Single-key reads only. | [optional] 
**message** | **str** | Single-key reads only. | [optional] 
**created_at** | **datetime** |  | [optional] 
**updated_at** | **datetime** |  | [optional] 
**expires_at** | **int** | Epoch seconds when the key expires. Absent when the key does not expire. | [optional] 
**version** | **str** | Format 2 stores only. A ULID, new on every write. Absent on ledger entries. | [optional] 
**ledger** | [**V2KvLedgerMeta**](V2KvLedgerMeta.md) |  | [optional] 
**personal** | **List[str]** | Ledger entries only: the personal fields that read \&quot;[PERSONAL]\&quot;. [\&quot;*\&quot;] when the whole value is hidden (the ledger definition could not be read). | [optional] 

## Example

```python
from quantcdn.models.v2_kv_entry import V2KvEntry

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvEntry from a JSON string
v2_kv_entry_instance = V2KvEntry.from_json(json)
# print the JSON string representation of the object
print(V2KvEntry.to_json())

# convert the object into a dict
v2_kv_entry_dict = v2_kv_entry_instance.to_dict()
# create an instance of V2KvEntry from a dict
v2_kv_entry_from_dict = V2KvEntry.from_dict(v2_kv_entry_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


