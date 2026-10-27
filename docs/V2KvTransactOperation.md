# V2KvTransactOperation

Each type takes only its own fields. check: version. set: value, secret, ttl, ifAbsent, ifVersion. delete: ifVersion. increment: amount (no ttl). Any other field fails VALIDATION.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **str** |  | 
**key** | **str** |  | 
**version** | **str** | check only: the key must have this version and not be expired. | [optional] 
**value** | **object** | set only. Any JSON value. | [optional] 
**secret** | **bool** | set only. Encrypt the value. | [optional] 
**ttl** | **int** | set only. Seconds (60 to 31,536,000). | [optional] 
**if_absent** | **bool** | set only. | [optional] 
**if_version** | **str** | set and delete. | [optional] 
**amount** | **int** | increment only. Nonzero. | [optional] [default to 1]

## Example

```python
from quantcdn.models.v2_kv_transact_operation import V2KvTransactOperation

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvTransactOperation from a JSON string
v2_kv_transact_operation_instance = V2KvTransactOperation.from_json(json)
# print the JSON string representation of the object
print(V2KvTransactOperation.to_json())

# convert the object into a dict
v2_kv_transact_operation_dict = v2_kv_transact_operation_instance.to_dict()
# create an instance of V2KvTransactOperation from a dict
v2_kv_transact_operation_from_dict = V2KvTransactOperation.from_dict(v2_kv_transact_operation_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


