# V2KvUpgradeState


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**format** | **int** |  | 
**state** | **str** | migrating while writes are frozen (an upgrade copy or a rollback). | 
**table** | **str** | The table that serves the store. | 
**upgrade** | [**V2KvUpgradeStatus**](V2KvUpgradeStatus.md) | Null when the store was never upgraded. | 

## Example

```python
from quantcdn.models.v2_kv_upgrade_state import V2KvUpgradeState

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvUpgradeState from a JSON string
v2_kv_upgrade_state_instance = V2KvUpgradeState.from_json(json)
# print the JSON string representation of the object
print(V2KvUpgradeState.to_json())

# convert the object into a dict
v2_kv_upgrade_state_dict = v2_kv_upgrade_state_instance.to_dict()
# create an instance of V2KvUpgradeState from a dict
v2_kv_upgrade_state_from_dict = V2KvUpgradeState.from_dict(v2_kv_upgrade_state_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


