# RestoreFilesystemRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**backup_id** | **str** | The backup ID to restore (must match path param) | 
**acknowledge_dataloss** | **bool** | Must be true. tar extraction overwrites same-named files in the target EFS in place; pre-existing files not in the archive are preserved. | 

## Example

```python
from quantcdn.models.restore_filesystem_request import RestoreFilesystemRequest

# TODO update the JSON string below
json = "{}"
# create an instance of RestoreFilesystemRequest from a JSON string
restore_filesystem_request_instance = RestoreFilesystemRequest.from_json(json)
# print the JSON string representation of the object
print(RestoreFilesystemRequest.to_json())

# convert the object into a dict
restore_filesystem_request_dict = restore_filesystem_request_instance.to_dict()
# create an instance of RestoreFilesystemRequest from a dict
restore_filesystem_request_from_dict = RestoreFilesystemRequest.from_dict(restore_filesystem_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


