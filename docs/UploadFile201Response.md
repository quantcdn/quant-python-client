# UploadFile201Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**file_id** | **str** |  | [optional] 
**s3_uri** | **str** | S3 URI (direct upload only) | [optional] 
**url** | **str** | Presigned download URL (direct upload only) | [optional] 
**upload_url** | **str** | Presigned PUT URL (presigned upload only) | [optional] 
**s3_key** | **str** | S3 object key (presigned upload only) | [optional] 
**expires_in** | **int** | URL expiry in seconds (presigned upload only) | [optional] 
**filename** | **str** |  | [optional] 
**content_type** | **str** |  | [optional] 
**size** | **int** |  | [optional] 
**metadata** | **object** |  | [optional] 
**created_at** | **datetime** |  | [optional] 

## Example

```python
from quantcdn.models.upload_file201_response import UploadFile201Response

# TODO update the JSON string below
json = "{}"
# create an instance of UploadFile201Response from a JSON string
upload_file201_response_instance = UploadFile201Response.from_json(json)
# print the JSON string representation of the object
print(UploadFile201Response.to_json())

# convert the object into a dict
upload_file201_response_dict = upload_file201_response_instance.to_dict()
# create an instance of UploadFile201Response from a dict
upload_file201_response_from_dict = UploadFile201Response.from_dict(upload_file201_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


