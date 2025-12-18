# V1Revision


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**md5** | **str** |  | [optional] 
**type** | **str** |  | [optional] 
**byte_length** | **int** |  | [optional] 
**revision_number** | **int** |  | [optional] 
**date_timestamp** | **int** |  | [optional] 
**deleted** | **bool** |  | [optional] 
**deleted_timestamp** | **int** |  | [optional] 
**transitions** | [**List[V1Transition]**](V1Transition.md) |  | [optional] 
**info** | [**V1Info**](V1Info.md) |  | [optional] 

## Example

```python
from quantcdn.models.v1_revision import V1Revision

# TODO update the JSON string below
json = "{}"
# create an instance of V1Revision from a JSON string
v1_revision_instance = V1Revision.from_json(json)
# print the JSON string representation of the object
print(V1Revision.to_json())

# convert the object into a dict
v1_revision_dict = v1_revision_instance.to_dict()
# create an instance of V1Revision from a dict
v1_revision_from_dict = V1Revision.from_dict(v1_revision_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


