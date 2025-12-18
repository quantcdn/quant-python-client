# Embeddings200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**embeddings** | [**Embeddings200ResponseEmbeddings**](Embeddings200ResponseEmbeddings.md) |  | 
**model** | **str** | Model used to generate embeddings | 
**dimension** | **int** | Dimensionality of each embedding vector | 
**usage** | [**Embeddings200ResponseUsage**](Embeddings200ResponseUsage.md) |  | 

## Example

```python
from quantcdn.models.embeddings200_response import Embeddings200Response

# TODO update the JSON string below
json = "{}"
# create an instance of Embeddings200Response from a JSON string
embeddings200_response_instance = Embeddings200Response.from_json(json)
# print the JSON string representation of the object
print(Embeddings200Response.to_json())

# convert the object into a dict
embeddings200_response_dict = embeddings200_response_instance.to_dict()
# create an instance of Embeddings200Response from a dict
embeddings200_response_from_dict = Embeddings200Response.from_dict(embeddings200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


