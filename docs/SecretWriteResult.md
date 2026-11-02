# SecretWriteResult


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**key** | **str** | The secret name | 
**warnings** | **List[str]** | Notices from Quant Cloud about the change. Present only when there is at least one. | [optional] 

## Example

```python
from quantcdn.models.secret_write_result import SecretWriteResult

# TODO update the JSON string below
json = "{}"
# create an instance of SecretWriteResult from a JSON string
secret_write_result_instance = SecretWriteResult.from_json(json)
# print the JSON string representation of the object
print(SecretWriteResult.to_json())

# convert the object into a dict
secret_write_result_dict = secret_write_result_instance.to_dict()
# create an instance of SecretWriteResult from a dict
secret_write_result_from_dict = SecretWriteResult.from_dict(secret_write_result_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


