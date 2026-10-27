# V2KvArchiveManifest

The pages that list every deleted object version. Each url is a signed download link valid 3,600 seconds.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**pages** | [**List[V2KvArchiveManifestPagesInner]**](V2KvArchiveManifestPagesInner.md) |  | [optional] 

## Example

```python
from quantcdn.models.v2_kv_archive_manifest import V2KvArchiveManifest

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvArchiveManifest from a JSON string
v2_kv_archive_manifest_instance = V2KvArchiveManifest.from_json(json)
# print the JSON string representation of the object
print(V2KvArchiveManifest.to_json())

# convert the object into a dict
v2_kv_archive_manifest_dict = v2_kv_archive_manifest_instance.to_dict()
# create an instance of V2KvArchiveManifest from a dict
v2_kv_archive_manifest_from_dict = V2KvArchiveManifest.from_dict(v2_kv_archive_manifest_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


