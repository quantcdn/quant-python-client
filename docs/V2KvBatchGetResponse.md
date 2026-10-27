# V2KvBatchGetResponse

One entry per requested key, in input order; null for a missing or expired key. The whole response is at most 4 MiB.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**items** | [**List[Optional[V2KvEntry]]**](V2KvEntry.md) |  | 

## Example

```python
from quantcdn.models.v2_kv_batch_get_response import V2KvBatchGetResponse

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvBatchGetResponse from a JSON string
v2_kv_batch_get_response_instance = V2KvBatchGetResponse.from_json(json)
# print the JSON string representation of the object
print(V2KvBatchGetResponse.to_json())

# convert the object into a dict
v2_kv_batch_get_response_dict = v2_kv_batch_get_response_instance.to_dict()
# create an instance of V2KvBatchGetResponse from a dict
v2_kv_batch_get_response_from_dict = V2KvBatchGetResponse.from_dict(v2_kv_batch_get_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


