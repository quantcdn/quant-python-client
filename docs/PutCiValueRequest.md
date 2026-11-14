# PutCiValueRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**kind** | **str** |  | 
**value** | **str** |  | 
**repo** | **str** | Owner/name. Lower-cased by the server. Leave out for an organisation value. | [optional] 
**branches** | **List[str]** | Only jobs on these branches get the value. Leave out for every branch. | [optional] 

## Example

```python
from quantcdn.models.put_ci_value_request import PutCiValueRequest

# TODO update the JSON string below
json = "{}"
# create an instance of PutCiValueRequest from a JSON string
put_ci_value_request_instance = PutCiValueRequest.from_json(json)
# print the JSON string representation of the object
print(PutCiValueRequest.to_json())

# convert the object into a dict
put_ci_value_request_dict = put_ci_value_request_instance.to_dict()
# create an instance of PutCiValueRequest from a dict
put_ci_value_request_from_dict = PutCiValueRequest.from_dict(put_ci_value_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


