# V1DeleteResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**error** | **bool** | Indicates at least one error occurred | [optional] 
**errors** | **List[object]** | List of any errors | [optional] 
**meta** | [**List[V1Revision]**](V1Revision.md) |  | [optional] 

## Example

```python
from quantcdn.models.v1_delete_response import V1DeleteResponse

# TODO update the JSON string below
json = "{}"
# create an instance of V1DeleteResponse from a JSON string
v1_delete_response_instance = V1DeleteResponse.from_json(json)
# print the JSON string representation of the object
print(V1DeleteResponse.to_json())

# convert the object into a dict
v1_delete_response_dict = v1_delete_response_instance.to_dict()
# create an instance of V1DeleteResponse from a dict
v1_delete_response_from_dict = V1DeleteResponse.from_dict(v1_delete_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


