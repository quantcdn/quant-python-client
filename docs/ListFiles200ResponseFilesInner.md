# ListFiles200ResponseFilesInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**file_id** | **str** |  | [optional] 
**filename** | **str** |  | [optional] 
**content_type** | **str** |  | [optional] 
**size** | **int** |  | [optional] 
**metadata** | **object** |  | [optional] 
**created_at** | **datetime** |  | [optional] 

## Example

```python
from quantcdn.models.list_files200_response_files_inner import ListFiles200ResponseFilesInner

# TODO update the JSON string below
json = "{}"
# create an instance of ListFiles200ResponseFilesInner from a JSON string
list_files200_response_files_inner_instance = ListFiles200ResponseFilesInner.from_json(json)
# print the JSON string representation of the object
print(ListFiles200ResponseFilesInner.to_json())

# convert the object into a dict
list_files200_response_files_inner_dict = list_files200_response_files_inner_instance.to_dict()
# create an instance of ListFiles200ResponseFilesInner from a dict
list_files200_response_files_inner_from_dict = ListFiles200ResponseFilesInner.from_dict(list_files200_response_files_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


