# UploadFileRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**content** | **str** | Base64-encoded file content (for direct upload). Required unless using requestUploadUrl. | [optional] 
**request_upload_url** | **bool** | Set to true to get a presigned S3 upload URL instead of uploading directly. | [optional] [default to False]
**size** | **int** | File size in bytes. Optional but recommended for presigned uploads. | [optional] 
**filename** | **str** | Original filename | [optional] 
**content_type** | **str** | MIME type of the file | 
**metadata** | **Dict[str, object]** | Custom metadata for filtering. Any fields allowed. | [optional] 

## Example

```python
from quantcdn.models.upload_file_request import UploadFileRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UploadFileRequest from a JSON string
upload_file_request_instance = UploadFileRequest.from_json(json)
# print the JSON string representation of the object
print(UploadFileRequest.to_json())

# convert the object into a dict
upload_file_request_dict = upload_file_request_instance.to_dict()
# create an instance of UploadFileRequest from a dict
upload_file_request_from_dict = UploadFileRequest.from_dict(upload_file_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


