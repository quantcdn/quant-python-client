# OaiEmbeddingsRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**model** | **str** |  | 
**input** | **object** | A string or array of strings to embed | 

## Example

```python
from quantcdn.models.oai_embeddings_request import OaiEmbeddingsRequest

# TODO update the JSON string below
json = "{}"
# create an instance of OaiEmbeddingsRequest from a JSON string
oai_embeddings_request_instance = OaiEmbeddingsRequest.from_json(json)
# print the JSON string representation of the object
print(OaiEmbeddingsRequest.to_json())

# convert the object into a dict
oai_embeddings_request_dict = oai_embeddings_request_instance.to_dict()
# create an instance of OaiEmbeddingsRequest from a dict
oai_embeddings_request_from_dict = OaiEmbeddingsRequest.from_dict(oai_embeddings_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


