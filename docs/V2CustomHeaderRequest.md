# V2CustomHeaderRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**headers** | **Dict[str, str]** | Custom headers | 

## Example

```python
from quantcdn.models.v2_custom_header_request import V2CustomHeaderRequest

# TODO update the JSON string below
json = "{}"
# create an instance of V2CustomHeaderRequest from a JSON string
v2_custom_header_request_instance = V2CustomHeaderRequest.from_json(json)
# print the JSON string representation of the object
print(V2CustomHeaderRequest.to_json())

# convert the object into a dict
v2_custom_header_request_dict = v2_custom_header_request_instance.to_dict()
# create an instance of V2CustomHeaderRequest from a dict
v2_custom_header_request_from_dict = V2CustomHeaderRequest.from_dict(v2_custom_header_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


