# V2KvCount


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**count** | **int** | Live keys that hold the value. A value that no key holds counts 0. | 

## Example

```python
from quantcdn.models.v2_kv_count import V2KvCount

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvCount from a JSON string
v2_kv_count_instance = V2KvCount.from_json(json)
# print the JSON string representation of the object
print(V2KvCount.to_json())

# convert the object into a dict
v2_kv_count_dict = v2_kv_count_instance.to_dict()
# create an instance of V2KvCount from a dict
v2_kv_count_from_dict = V2KvCount.from_dict(v2_kv_count_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


