# CiCacheDeleteResult


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**deleted_entries** | **int** |  | 
**deleted_bytes** | **int** |  | 
**complete** | **bool** | false when the delete stopped at its time limit (about 12 seconds), a storage call failed or timed out, or storage refused some objects. false means: send the same request again until it is true. If a call returns false with deletedEntries 0, stop and try again later, because a storage call failed, timed out or refused objects. | 

## Example

```python
from quantcdn.models.ci_cache_delete_result import CiCacheDeleteResult

# TODO update the JSON string below
json = "{}"
# create an instance of CiCacheDeleteResult from a JSON string
ci_cache_delete_result_instance = CiCacheDeleteResult.from_json(json)
# print the JSON string representation of the object
print(CiCacheDeleteResult.to_json())

# convert the object into a dict
ci_cache_delete_result_dict = ci_cache_delete_result_instance.to_dict()
# create an instance of CiCacheDeleteResult from a dict
ci_cache_delete_result_from_dict = CiCacheDeleteResult.from_dict(ci_cache_delete_result_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


