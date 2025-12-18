# V1RevisionsResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**revisions** | **object** | Revision objects, mapped by revision number | [optional] 
**url** | **str** | The url of the asset | [optional] 
**published** | **bool** | Published state of the asset | [optional] 
**published_revision** | **int** | Published revision number of the asset | [optional] 
**transitions** | [**List[V1Transition]**](V1Transition.md) |  | [optional] 
**highest_revision_number** | **int** | Last revision number | [optional] 
**transition_revision** | **int** | The transition number, if set | [optional] 

## Example

```python
from quantcdn.models.v1_revisions_response import V1RevisionsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of V1RevisionsResponse from a JSON string
v1_revisions_response_instance = V1RevisionsResponse.from_json(json)
# print the JSON string representation of the object
print(V1RevisionsResponse.to_json())

# convert the object into a dict
v1_revisions_response_dict = v1_revisions_response_instance.to_dict()
# create an instance of V1RevisionsResponse from a dict
v1_revisions_response_from_dict = V1RevisionsResponse.from_dict(v1_revisions_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


