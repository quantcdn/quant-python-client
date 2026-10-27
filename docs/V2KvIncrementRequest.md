# V2KvIncrementRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**amount** | **int** | A nonzero integer. The result must stay a safe integer. | [optional] [default to 1]
**ttl** | **int** | Seconds (60 to 31,536,000). Applied only when the key is created or reset after expiry. | [optional] 

## Example

```python
from quantcdn.models.v2_kv_increment_request import V2KvIncrementRequest

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvIncrementRequest from a JSON string
v2_kv_increment_request_instance = V2KvIncrementRequest.from_json(json)
# print the JSON string representation of the object
print(V2KvIncrementRequest.to_json())

# convert the object into a dict
v2_kv_increment_request_dict = v2_kv_increment_request_instance.to_dict()
# create an instance of V2KvIncrementRequest from a dict
v2_kv_increment_request_from_dict = V2KvIncrementRequest.from_dict(v2_kv_increment_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


