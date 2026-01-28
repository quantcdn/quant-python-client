# GetFile200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**file_id** | **str** |  | [optional] 
**s3_uri** | **str** |  | [optional] 
**url** | **str** | Presigned download URL (1 hour) | [optional] 
**filename** | **str** |  | [optional] 
**content_type** | **str** |  | [optional] 
**size** | **int** |  | [optional] 
**metadata** | **object** |  | [optional] 
**created_at** | **datetime** |  | [optional] 

## Example

```python
from quantcdn.models.get_file200_response import GetFile200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetFile200Response from a JSON string
get_file200_response_instance = GetFile200Response.from_json(json)
# print the JSON string representation of the object
print(GetFile200Response.to_json())

# convert the object into a dict
get_file200_response_dict = get_file200_response_instance.to_dict()
# create an instance of GetFile200Response from a dict
get_file200_response_from_dict = GetFile200Response.from_dict(get_file200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


