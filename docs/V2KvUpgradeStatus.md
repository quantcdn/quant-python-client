# V2KvUpgradeStatus

The latest format 1 to format 2 upgrade. Phases with a running step: preflight, creating, freezing, copying, verifying, rollback_freezing, rolling_back. Terminal: checked (dry run), failed, rolled_back, finalized. switched waits for rollback or finalize.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**phase** | **str** | The current upgrade phase. | 
**dry_run** | **bool** |  | 
**v1_table** | **str** |  | 
**v2_table** | **str** |  | 
**started_at** | **datetime** |  | 
**frozen_at** | **datetime** | When writes were last frozen. | [optional] 
**switched_at** | **datetime** |  | [optional] 
**retain_until** | **datetime** | The format 1 table is kept until this time (14 days after the switch); finalize is allowed after it. | [optional] 
**total** | **int** | Items counted by preflight. | [optional] 
**copied** | **int** | Items copied so far. | [optional] 
**invalid_keys** | **List[str]** | Up to 20 keys that are not valid in format 2 (preflight). | [optional] 
**oversize_keys** | **List[str]** | Up to 20 keys whose items would exceed the 400 KB item limit in format 2 (preflight). | [optional] 
**error** | **str** | Why the upgrade failed. | [optional] 

## Example

```python
from quantcdn.models.v2_kv_upgrade_status import V2KvUpgradeStatus

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvUpgradeStatus from a JSON string
v2_kv_upgrade_status_instance = V2KvUpgradeStatus.from_json(json)
# print the JSON string representation of the object
print(V2KvUpgradeStatus.to_json())

# convert the object into a dict
v2_kv_upgrade_status_dict = v2_kv_upgrade_status_instance.to_dict()
# create an instance of V2KvUpgradeStatus from a dict
v2_kv_upgrade_status_from_dict = V2KvUpgradeStatus.from_dict(v2_kv_upgrade_status_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


