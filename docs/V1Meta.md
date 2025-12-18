# V1Meta


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url** | **str** |  | [optional] 
**type** | **str** |  | [optional] 
**seq_num** | **int** |  | [optional] 
**published** | **bool** |  | [optional] 
**published_revision** | **int** |  | [optional] 
**published_md5** | **str** |  | [optional] 
**byte_length** | **int** |  | [optional] 
**revision_count** | **int** |  | [optional] 
**highest_revision_number** | **int** |  | [optional] 
**deleted** | **bool** |  | [optional] 
**deleted_timestamp** | **int** |  | [optional] 
**md5** | **str** |  | [optional] 
**revision_number** | **int** |  | [optional] 
**date_timestamp** | **int** |  | [optional] 

## Example

```python
from quantcdn.models.v1_meta import V1Meta

# TODO update the JSON string below
json = "{}"
# create an instance of V1Meta from a JSON string
v1_meta_instance = V1Meta.from_json(json)
# print the JSON string representation of the object
print(V1Meta.to_json())

# convert the object into a dict
v1_meta_dict = v1_meta_instance.to_dict()
# create an instance of V1Meta from a dict
v1_meta_from_dict = V1Meta.from_dict(v1_meta_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


