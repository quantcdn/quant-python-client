# V2KvExportDownload


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**part** | **int** |  | 
**url** | **str** | Presigned URL, valid for 1 hour, new on every call. | 
**size_bytes** | **int** |  | 

## Example

```python
from quantcdn.models.v2_kv_export_download import V2KvExportDownload

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvExportDownload from a JSON string
v2_kv_export_download_instance = V2KvExportDownload.from_json(json)
# print the JSON string representation of the object
print(V2KvExportDownload.to_json())

# convert the object into a dict
v2_kv_export_download_dict = v2_kv_export_download_instance.to_dict()
# create an instance of V2KvExportDownload from a dict
v2_kv_export_download_from_dict = V2KvExportDownload.from_dict(v2_kv_export_download_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


