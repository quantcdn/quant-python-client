# V1UploadResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | 
**url** | **str** |  | 

## Example

```python
from quantcdn.models.v1_upload_response import V1UploadResponse

# TODO update the JSON string below
json = "{}"
# create an instance of V1UploadResponse from a JSON string
v1_upload_response_instance = V1UploadResponse.from_json(json)
# print the JSON string representation of the object
print(V1UploadResponse.to_json())

# convert the object into a dict
v1_upload_response_dict = v1_upload_response_instance.to_dict()
# create an instance of V1UploadResponse from a dict
v1_upload_response_from_dict = V1UploadResponse.from_dict(v1_upload_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


