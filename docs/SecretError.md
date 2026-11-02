# SecretError


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | 

## Example

```python
from quantcdn.models.secret_error import SecretError

# TODO update the JSON string below
json = "{}"
# create an instance of SecretError from a JSON string
secret_error_instance = SecretError.from_json(json)
# print the JSON string representation of the object
print(SecretError.to_json())

# convert the object into a dict
secret_error_dict = secret_error_instance.to_dict()
# create an instance of SecretError from a dict
secret_error_from_dict = SecretError.from_dict(secret_error_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


