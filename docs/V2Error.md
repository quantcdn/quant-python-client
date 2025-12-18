# V2Error


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** | Error message | 
**error** | **bool** | Error flag | 

## Example

```python
from quantcdn.models.v2_error import V2Error

# TODO update the JSON string below
json = "{}"
# create an instance of V2Error from a JSON string
v2_error_instance = V2Error.from_json(json)
# print the JSON string representation of the object
print(V2Error.to_json())

# convert the object into a dict
v2_error_dict = v2_error_instance.to_dict()
# create an instance of V2Error from a dict
v2_error_from_dict = V2Error.from_dict(v2_error_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


