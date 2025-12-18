# Embeddings200ResponseEmbeddings

Vector embeddings for the input text(s). Single array for string input, array of arrays for batch input.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------

## Example

```python
from quantcdn.models.embeddings200_response_embeddings import Embeddings200ResponseEmbeddings

# TODO update the JSON string below
json = "{}"
# create an instance of Embeddings200ResponseEmbeddings from a JSON string
embeddings200_response_embeddings_instance = Embeddings200ResponseEmbeddings.from_json(json)
# print the JSON string representation of the object
print(Embeddings200ResponseEmbeddings.to_json())

# convert the object into a dict
embeddings200_response_embeddings_dict = embeddings200_response_embeddings_instance.to_dict()
# create an instance of Embeddings200ResponseEmbeddings from a dict
embeddings200_response_embeddings_from_dict = Embeddings200ResponseEmbeddings.from_dict(embeddings200_response_embeddings_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


