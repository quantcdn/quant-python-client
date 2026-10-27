# V2KvArchiveManifestPagesInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**key** | **str** |  | [optional] 
**version_id** | **str** |  | [optional] 
**sha256** | **str** |  | [optional] 
**count** | **int** |  | [optional] 
**url** | **str** |  | [optional] 
**expires_at** | **datetime** |  | [optional] 

## Example

```python
from quantcdn.models.v2_kv_archive_manifest_pages_inner import V2KvArchiveManifestPagesInner

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvArchiveManifestPagesInner from a JSON string
v2_kv_archive_manifest_pages_inner_instance = V2KvArchiveManifestPagesInner.from_json(json)
# print the JSON string representation of the object
print(V2KvArchiveManifestPagesInner.to_json())

# convert the object into a dict
v2_kv_archive_manifest_pages_inner_dict = v2_kv_archive_manifest_pages_inner_instance.to_dict()
# create an instance of V2KvArchiveManifestPagesInner from a dict
v2_kv_archive_manifest_pages_inner_from_dict = V2KvArchiveManifestPagesInner.from_dict(v2_kv_archive_manifest_pages_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


