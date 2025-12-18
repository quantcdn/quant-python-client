# CreateApplicationRequestFilesystem

Optional filesystem configuration

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**required** | **bool** | Whether to create a shared filesystem | [optional] [default to True]
**mount_path** | **str** | Mount path inside containers | [optional] [default to '/mnt/data']

## Example

```python
from quantcdn.models.create_application_request_filesystem import CreateApplicationRequestFilesystem

# TODO update the JSON string below
json = "{}"
# create an instance of CreateApplicationRequestFilesystem from a JSON string
create_application_request_filesystem_instance = CreateApplicationRequestFilesystem.from_json(json)
# print the JSON string representation of the object
print(CreateApplicationRequestFilesystem.to_json())

# convert the object into a dict
create_application_request_filesystem_dict = create_application_request_filesystem_instance.to_dict()
# create an instance of CreateApplicationRequestFilesystem from a dict
create_application_request_filesystem_from_dict = CreateApplicationRequestFilesystem.from_dict(create_application_request_filesystem_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


