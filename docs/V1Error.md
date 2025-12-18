# V1Error


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**error** | **bool** |  | 
**message** | **str** |  | 

## Example

```python
from quantcdn.models.v1_error import V1Error

# TODO update the JSON string below
json = "{}"
# create an instance of V1Error from a JSON string
v1_error_instance = V1Error.from_json(json)
# print the JSON string representation of the object
print(V1Error.to_json())

# convert the object into a dict
v1_error_dict = v1_error_instance.to_dict()
# create an instance of V1Error from a dict
v1_error_from_dict = V1Error.from_dict(v1_error_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


