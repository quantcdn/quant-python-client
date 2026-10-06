# OaiEmbeddings200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**object** | **str** |  | [optional] 
**data** | [**List[OaiEmbeddings200ResponseDataInner]**](OaiEmbeddings200ResponseDataInner.md) |  | [optional] 
**model** | **str** |  | [optional] 
**usage** | [**OaiEmbeddings200ResponseUsage**](OaiEmbeddings200ResponseUsage.md) |  | [optional] 

## Example

```python
from quantcdn.models.oai_embeddings200_response import OaiEmbeddings200Response

# TODO update the JSON string below
json = "{}"
# create an instance of OaiEmbeddings200Response from a JSON string
oai_embeddings200_response_instance = OaiEmbeddings200Response.from_json(json)
# print the JSON string representation of the object
print(OaiEmbeddings200Response.to_json())

# convert the object into a dict
oai_embeddings200_response_dict = oai_embeddings200_response_instance.to_dict()
# create an instance of OaiEmbeddings200Response from a dict
oai_embeddings200_response_from_dict = OaiEmbeddings200Response.from_dict(oai_embeddings200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


