# CiCacheDeleteRequest

The scope to delete: either {\"all\": true} alone (the whole cache of the pool), or repoId with optionally ref, version and key, where a field needs every field before it (repoId, ref, version, key). An empty object is refused.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**all** | **bool** | true clears the whole cache of the pool. Must be the only field. | [optional] 
**repo_id** | **int** | GitHub repository id. A digit string is also accepted. | [optional] 
**ref** | **str** | Git ref; starts with refs/, a valid git ref name without %. | [optional] 
**version** | **str** |  | [optional] 
**key** | **str** | The exact cache key. Deletes only that entry, not keys that start with it. | [optional] 

## Example

```python
from quantcdn.models.ci_cache_delete_request import CiCacheDeleteRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CiCacheDeleteRequest from a JSON string
ci_cache_delete_request_instance = CiCacheDeleteRequest.from_json(json)
# print the JSON string representation of the object
print(CiCacheDeleteRequest.to_json())

# convert the object into a dict
ci_cache_delete_request_dict = ci_cache_delete_request_instance.to_dict()
# create an instance of CiCacheDeleteRequest from a dict
ci_cache_delete_request_from_dict = CiCacheDeleteRequest.from_dict(ci_cache_delete_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


