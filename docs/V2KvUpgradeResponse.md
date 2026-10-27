# V2KvUpgradeResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**upgrade** | [**V2KvUpgradeStatus**](V2KvUpgradeStatus.md) |  | 

## Example

```python
from quantcdn.models.v2_kv_upgrade_response import V2KvUpgradeResponse

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvUpgradeResponse from a JSON string
v2_kv_upgrade_response_instance = V2KvUpgradeResponse.from_json(json)
# print the JSON string representation of the object
print(V2KvUpgradeResponse.to_json())

# convert the object into a dict
v2_kv_upgrade_response_dict = v2_kv_upgrade_response_instance.to_dict()
# create an instance of V2KvUpgradeResponse from a dict
v2_kv_upgrade_response_from_dict = V2KvUpgradeResponse.from_dict(v2_kv_upgrade_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


