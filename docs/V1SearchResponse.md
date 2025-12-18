# V1SearchResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**settings** | **object** | Search configuration for the index | [optional] 
**index** | **object** | Detail related to index size and status | [optional] 

## Example

```python
from quantcdn.models.v1_search_response import V1SearchResponse

# TODO update the JSON string below
json = "{}"
# create an instance of V1SearchResponse from a JSON string
v1_search_response_instance = V1SearchResponse.from_json(json)
# print the JSON string representation of the object
print(V1SearchResponse.to_json())

# convert the object into a dict
v1_search_response_dict = v1_search_response_instance.to_dict()
# create an instance of V1SearchResponse from a dict
v1_search_response_from_dict = V1SearchResponse.from_dict(v1_search_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


