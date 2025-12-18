# V1RedirectRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url** | **str** | The redirect from URL | 
**redirect_url** | **str** | The destination URL | 
**redirect_http_code** | **int** | The HTTP code to send with the redirect | 
**published** | **bool** | If the redirect is published | 
**content_timestamp** | **int** | User defined timestamp for this content item | [optional] 
**info** | [**V1Info**](V1Info.md) |  | [optional] 
**transitions** | [**List[V1Transition]**](V1Transition.md) |  | [optional] 

## Example

```python
from quantcdn.models.v1_redirect_request import V1RedirectRequest

# TODO update the JSON string below
json = "{}"
# create an instance of V1RedirectRequest from a JSON string
v1_redirect_request_instance = V1RedirectRequest.from_json(json)
# print the JSON string representation of the object
print(V1RedirectRequest.to_json())

# convert the object into a dict
v1_redirect_request_dict = v1_redirect_request_instance.to_dict()
# create an instance of V1RedirectRequest from a dict
v1_redirect_request_from_dict = V1RedirectRequest.from_dict(v1_redirect_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


