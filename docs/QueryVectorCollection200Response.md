# QueryVectorCollection200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**results** | [**List[QueryVectorCollection200ResponseResultsInner]**](QueryVectorCollection200ResponseResultsInner.md) |  | [optional] 
**query** | **str** |  | [optional] 
**count** | **int** |  | [optional] 
**execution_time_ms** | **int** |  | [optional] 

## Example

```python
from quantcdn.models.query_vector_collection200_response import QueryVectorCollection200Response

# TODO update the JSON string below
json = "{}"
# create an instance of QueryVectorCollection200Response from a JSON string
query_vector_collection200_response_instance = QueryVectorCollection200Response.from_json(json)
# print the JSON string representation of the object
print(QueryVectorCollection200Response.to_json())

# convert the object into a dict
query_vector_collection200_response_dict = query_vector_collection200_response_instance.to_dict()
# create an instance of QueryVectorCollection200Response from a dict
query_vector_collection200_response_from_dict = QueryVectorCollection200Response.from_dict(query_vector_collection200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


