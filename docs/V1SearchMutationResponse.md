# V1SearchMutationResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | 
**message** | **str** |  | 
**result** | **object** |  | [optional] 

## Example

```python
from quantcdn.models.v1_search_mutation_response import V1SearchMutationResponse

# TODO update the JSON string below
json = "{}"
# create an instance of V1SearchMutationResponse from a JSON string
v1_search_mutation_response_instance = V1SearchMutationResponse.from_json(json)
# print the JSON string representation of the object
print(V1SearchMutationResponse.to_json())

# convert the object into a dict
v1_search_mutation_response_dict = v1_search_mutation_response_instance.to_dict()
# create an instance of V1SearchMutationResponse from a dict
v1_search_mutation_response_from_dict = V1SearchMutationResponse.from_dict(v1_search_mutation_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


