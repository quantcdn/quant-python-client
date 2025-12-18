# EmbeddingsRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**input** | [**EmbeddingsRequestInput**](EmbeddingsRequestInput.md) |  | 
**model_id** | **str** | Embedding model to use | [optional] [default to 'amazon.titan-embed-text-v2:0']
**dimensions** | **int** | Output embedding dimensions. Titan v2 supports: 256, 512, 1024, 8192 | [optional] [default to 1024]
**normalize** | **bool** | Normalize embeddings to unit length (magnitude &#x3D; 1.0) | [optional] [default to True]

## Example

```python
from quantcdn.models.embeddings_request import EmbeddingsRequest

# TODO update the JSON string below
json = "{}"
# create an instance of EmbeddingsRequest from a JSON string
embeddings_request_instance = EmbeddingsRequest.from_json(json)
# print the JSON string representation of the object
print(EmbeddingsRequest.to_json())

# convert the object into a dict
embeddings_request_dict = embeddings_request_instance.to_dict()
# create an instance of EmbeddingsRequest from a dict
embeddings_request_from_dict = EmbeddingsRequest.from_dict(embeddings_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


