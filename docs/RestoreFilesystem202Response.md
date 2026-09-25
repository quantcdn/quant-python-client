# RestoreFilesystem202Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**restore_id** | **str** |  | [optional] 
**status** | **str** |  | [optional] 
**message** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.restore_filesystem202_response import RestoreFilesystem202Response

# TODO update the JSON string below
json = "{}"
# create an instance of RestoreFilesystem202Response from a JSON string
restore_filesystem202_response_instance = RestoreFilesystem202Response.from_json(json)
# print the JSON string representation of the object
print(RestoreFilesystem202Response.to_json())

# convert the object into a dict
restore_filesystem202_response_dict = restore_filesystem202_response_instance.to_dict()
# create an instance of RestoreFilesystem202Response from a dict
restore_filesystem202_response_from_dict = RestoreFilesystem202Response.from_dict(restore_filesystem202_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


