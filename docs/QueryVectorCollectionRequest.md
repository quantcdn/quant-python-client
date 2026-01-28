# QueryVectorCollectionRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**query** | **str** | Natural language search query (mutually exclusive with vector) | [optional] 
**vector** | **List[float]** | Pre-computed embedding vector (mutually exclusive with query). Array length must match collection dimension. | [optional] 
**limit** | **int** | Maximum number of results to return | [optional] [default to 5]
**threshold** | **float** | Minimum similarity score (0-1, higher &#x3D; more relevant) | [optional] [default to 0.7]
**include_embeddings** | **bool** | Include embedding vectors in response (for debugging) | [optional] [default to False]
**filter** | [**QueryVectorCollectionRequestFilter**](QueryVectorCollectionRequestFilter.md) |  | [optional] 
**list_by_metadata** | **bool** | If true, skip semantic search and return all documents matching the filter. Requires filter. Supports cursor pagination. | [optional] [default to False]
**cursor** | **str** | Pagination cursor for listByMetadata mode. Use nextCursor from previous response. Opaque format - do not construct manually. | [optional] 
**sort_by** | **str** | Field to sort by in listByMetadata mode | [optional] [default to 'created_at']
**sort_order** | **str** | Sort direction in listByMetadata mode | [optional] [default to 'desc']

## Example

```python
from quantcdn.models.query_vector_collection_request import QueryVectorCollectionRequest

# TODO update the JSON string below
json = "{}"
# create an instance of QueryVectorCollectionRequest from a JSON string
query_vector_collection_request_instance = QueryVectorCollectionRequest.from_json(json)
# print the JSON string representation of the object
print(QueryVectorCollectionRequest.to_json())

# convert the object into a dict
query_vector_collection_request_dict = query_vector_collection_request_instance.to_dict()
# create an instance of QueryVectorCollectionRequest from a dict
query_vector_collection_request_from_dict = QueryVectorCollectionRequest.from_dict(query_vector_collection_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


