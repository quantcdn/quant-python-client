# QueryVectorCollectionRequestFilter

Filter results by metadata fields. Applied AFTER semantic search (or alone in listByMetadata mode). All conditions use AND logic.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**exact** | **Dict[str, object]** | Exact match on metadata fields. Keys are metadata field names, values are expected values. | [optional] 
**contains** | **Dict[str, List[str]]** | Array contains filter for array metadata fields (like tags). Returns documents where the metadata array contains ANY of the specified values. | [optional] 

## Example

```python
from quantcdn.models.query_vector_collection_request_filter import QueryVectorCollectionRequestFilter

# TODO update the JSON string below
json = "{}"
# create an instance of QueryVectorCollectionRequestFilter from a JSON string
query_vector_collection_request_filter_instance = QueryVectorCollectionRequestFilter.from_json(json)
# print the JSON string representation of the object
print(QueryVectorCollectionRequestFilter.to_json())

# convert the object into a dict
query_vector_collection_request_filter_dict = query_vector_collection_request_filter_instance.to_dict()
# create an instance of QueryVectorCollectionRequestFilter from a dict
query_vector_collection_request_filter_from_dict = QueryVectorCollectionRequestFilter.from_dict(query_vector_collection_request_filter_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


