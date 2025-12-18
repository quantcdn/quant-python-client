# V1RedirectResponse


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
**redirect_http_code** | **int** | The HTTP code | [optional] 
**highest_revision_number** | **str** |  | [optional] 
**url** | **str** | The redirect from URL | [optional] 

## Example

```python
from quantcdn.models.v1_redirect_response import V1RedirectResponse

# TODO update the JSON string below
json = "{}"
# create an instance of V1RedirectResponse from a JSON string
v1_redirect_response_instance = V1RedirectResponse.from_json(json)
# print the JSON string representation of the object
print(V1RedirectResponse.to_json())

# convert the object into a dict
v1_redirect_response_dict = v1_redirect_response_instance.to_dict()
# create an instance of V1RedirectResponse from a dict
v1_redirect_response_from_dict = V1RedirectResponse.from_dict(v1_redirect_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


