# DownloadBackup200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**download_url** | **str** | Pre-signed S3 URL for download | [optional] 
**expires_at** | **datetime** | URL expiration time | [optional] 
**filename** | **str** | Suggested filename for download | [optional] 

## Example

```python
from quantcdn.models.download_backup200_response import DownloadBackup200Response

# TODO update the JSON string below
json = "{}"
# create an instance of DownloadBackup200Response from a JSON string
download_backup200_response_instance = DownloadBackup200Response.from_json(json)
# print the JSON string representation of the object
print(DownloadBackup200Response.to_json())

# convert the object into a dict
download_backup200_response_dict = download_backup200_response_instance.to_dict()
# create an instance of DownloadBackup200Response from a dict
download_backup200_response_from_dict = DownloadBackup200Response.from_dict(download_backup200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


