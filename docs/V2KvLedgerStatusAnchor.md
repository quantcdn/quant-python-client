# V2KvLedgerStatusAnchor


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **str** |  | 
**last_day** | **str** |  | [optional] 
**failing_since** | **datetime** |  | [optional] 
**error** | **str** |  | [optional] 
**bucket_policy** | **str** | customer-bucket only: the bucket policy (JSON) that lets Quant write the witness copies. | [optional] 

## Example

```python
from quantcdn.models.v2_kv_ledger_status_anchor import V2KvLedgerStatusAnchor

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvLedgerStatusAnchor from a JSON string
v2_kv_ledger_status_anchor_instance = V2KvLedgerStatusAnchor.from_json(json)
# print the JSON string representation of the object
print(V2KvLedgerStatusAnchor.to_json())

# convert the object into a dict
v2_kv_ledger_status_anchor_dict = v2_kv_ledger_status_anchor_instance.to_dict()
# create an instance of V2KvLedgerStatusAnchor from a dict
v2_kv_ledger_status_anchor_from_dict = V2KvLedgerStatusAnchor.from_dict(v2_kv_ledger_status_anchor_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


