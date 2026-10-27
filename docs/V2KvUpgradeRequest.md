# V2KvUpgradeRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**action** | **str** | start: preflight, copy and switch to format 2. rollback: copy back to format 1 after the switch. finalize: delete the format 1 table after retainUntil; no rollback is possible after it. resume: queue the current step again when the phase has not changed for more than 960 seconds. | 
**dry_run** | **bool** | start only: run preflight and stop at phase checked. Must be a JSON boolean. | [optional] [default to False]

## Example

```python
from quantcdn.models.v2_kv_upgrade_request import V2KvUpgradeRequest

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvUpgradeRequest from a JSON string
v2_kv_upgrade_request_instance = V2KvUpgradeRequest.from_json(json)
# print the JSON string representation of the object
print(V2KvUpgradeRequest.to_json())

# convert the object into a dict
v2_kv_upgrade_request_dict = v2_kv_upgrade_request_instance.to_dict()
# create an instance of V2KvUpgradeRequest from a dict
v2_kv_upgrade_request_from_dict = V2KvUpgradeRequest.from_dict(v2_kv_upgrade_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


