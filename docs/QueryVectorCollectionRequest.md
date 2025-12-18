# QueryVectorCollectionRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**query** | **str** | Natural language search query | 
**count** | **int** | Number of results to return | [optional] [default to 5]

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


