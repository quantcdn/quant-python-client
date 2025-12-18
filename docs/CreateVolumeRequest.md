# CreateVolumeRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**volume_name** | **str** | Volume name | 
**description** | **str** | Volume description | [optional] 
**root_directory** | **str** | Root directory path | [optional] 

## Example

```python
from quantcdn.models.create_volume_request import CreateVolumeRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateVolumeRequest from a JSON string
create_volume_request_instance = CreateVolumeRequest.from_json(json)
# print the JSON string representation of the object
print(CreateVolumeRequest.to_json())

# convert the object into a dict
create_volume_request_dict = create_volume_request_instance.to_dict()
# create an instance of CreateVolumeRequest from a dict
create_volume_request_from_dict = CreateVolumeRequest.from_dict(create_volume_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


