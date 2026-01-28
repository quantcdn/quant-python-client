# DeleteFile200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | [optional] 
**file_id** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.delete_file200_response import DeleteFile200Response

# TODO update the JSON string below
json = "{}"
# create an instance of DeleteFile200Response from a JSON string
delete_file200_response_instance = DeleteFile200Response.from_json(json)
# print the JSON string representation of the object
print(DeleteFile200Response.to_json())

# convert the object into a dict
delete_file200_response_dict = delete_file200_response_instance.to_dict()
# create an instance of DeleteFile200Response from a dict
delete_file200_response_from_dict = DeleteFile200Response.from_dict(delete_file200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


