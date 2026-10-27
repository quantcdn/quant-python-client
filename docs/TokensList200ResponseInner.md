# TokensList200ResponseInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | [optional] 
**name** | **str** |  | [optional] 
**last_used** | **datetime** |  | [optional] 
**created_at** | **datetime** |  | [optional] 

## Example

```python
from quantcdn.models.tokens_list200_response_inner import TokensList200ResponseInner

# TODO update the JSON string below
json = "{}"
# create an instance of TokensList200ResponseInner from a JSON string
tokens_list200_response_inner_instance = TokensList200ResponseInner.from_json(json)
# print the JSON string representation of the object
print(TokensList200ResponseInner.to_json())

# convert the object into a dict
tokens_list200_response_inner_dict = tokens_list200_response_inner_instance.to_dict()
# create an instance of TokensList200ResponseInner from a dict
tokens_list200_response_inner_from_dict = TokensList200ResponseInner.from_dict(tokens_list200_response_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


