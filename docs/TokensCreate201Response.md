# TokensCreate201Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**token** | **str** | The plain text token (shown once) | [optional] 
**id** | **int** | Token ID | [optional] 
**name** | **str** |  | [optional] 
**scopes** | **List[str]** |  | [optional] 
**projects** | **List[int]** |  | [optional] 
**preset** | **str** |  | [optional] 
**expires_at** | **datetime** |  | [optional] 
**created_at** | **datetime** |  | [optional] 

## Example

```python
from quantcdn.models.tokens_create201_response import TokensCreate201Response

# TODO update the JSON string below
json = "{}"
# create an instance of TokensCreate201Response from a JSON string
tokens_create201_response_instance = TokensCreate201Response.from_json(json)
# print the JSON string representation of the object
print(TokensCreate201Response.to_json())

# convert the object into a dict
tokens_create201_response_dict = tokens_create201_response_instance.to_dict()
# create an instance of TokensCreate201Response from a dict
tokens_create201_response_from_dict = TokensCreate201Response.from_dict(tokens_create201_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


