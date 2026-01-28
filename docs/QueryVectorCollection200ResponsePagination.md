# QueryVectorCollection200ResponsePagination

Pagination info (listByMetadata mode only)

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**sort_by** | **str** |  | [optional] 
**sort_order** | **str** |  | [optional] 
**limit** | **int** |  | [optional] 

## Example

```python
from quantcdn.models.query_vector_collection200_response_pagination import QueryVectorCollection200ResponsePagination

# TODO update the JSON string below
json = "{}"
# create an instance of QueryVectorCollection200ResponsePagination from a JSON string
query_vector_collection200_response_pagination_instance = QueryVectorCollection200ResponsePagination.from_json(json)
# print the JSON string representation of the object
print(QueryVectorCollection200ResponsePagination.to_json())

# convert the object into a dict
query_vector_collection200_response_pagination_dict = query_vector_collection200_response_pagination_instance.to_dict()
# create an instance of QueryVectorCollection200ResponsePagination from a dict
query_vector_collection200_response_pagination_from_dict = QueryVectorCollection200ResponsePagination.from_dict(query_vector_collection200_response_pagination_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


