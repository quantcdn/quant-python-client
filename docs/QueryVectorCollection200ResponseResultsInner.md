# QueryVectorCollection200ResponseResultsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**content** | **str** |  | [optional] 
**score** | **float** |  | [optional] 
**metadata** | [**QueryVectorCollection200ResponseResultsInnerMetadata**](QueryVectorCollection200ResponseResultsInnerMetadata.md) |  | [optional] 

## Example

```python
from quantcdn.models.query_vector_collection200_response_results_inner import QueryVectorCollection200ResponseResultsInner

# TODO update the JSON string below
json = "{}"
# create an instance of QueryVectorCollection200ResponseResultsInner from a JSON string
query_vector_collection200_response_results_inner_instance = QueryVectorCollection200ResponseResultsInner.from_json(json)
# print the JSON string representation of the object
print(QueryVectorCollection200ResponseResultsInner.to_json())

# convert the object into a dict
query_vector_collection200_response_results_inner_dict = query_vector_collection200_response_results_inner_instance.to_dict()
# create an instance of QueryVectorCollection200ResponseResultsInner from a dict
query_vector_collection200_response_results_inner_from_dict = QueryVectorCollection200ResponseResultsInner.from_dict(query_vector_collection200_response_results_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


