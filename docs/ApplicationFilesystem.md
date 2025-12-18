# ApplicationFilesystem

Filesystem configuration

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**filesystem_id** | **str** | EFS filesystem ID | [optional] 
**mount_path** | **str** | Default mount path in containers | [optional] 

## Example

```python
from quantcdn.models.application_filesystem import ApplicationFilesystem

# TODO update the JSON string below
json = "{}"
# create an instance of ApplicationFilesystem from a JSON string
application_filesystem_instance = ApplicationFilesystem.from_json(json)
# print the JSON string representation of the object
print(ApplicationFilesystem.to_json())

# convert the object into a dict
application_filesystem_dict = application_filesystem_instance.to_dict()
# create an instance of ApplicationFilesystem from a dict
application_filesystem_from_dict = ApplicationFilesystem.from_dict(application_filesystem_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


