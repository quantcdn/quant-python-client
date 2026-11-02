# SecretKey


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**key** | **str** | The secret name | 

## Example

```python
from quantcdn.models.secret_key import SecretKey

# TODO update the JSON string below
json = "{}"
# create an instance of SecretKey from a JSON string
secret_key_instance = SecretKey.from_json(json)
# print the JSON string representation of the object
print(SecretKey.to_json())

# convert the object into a dict
secret_key_dict = secret_key_instance.to_dict()
# create an instance of SecretKey from a dict
secret_key_from_dict = SecretKey.from_dict(secret_key_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


