# OaiEmbeddings200ResponseDataInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**object** | **str** |  | [optional] 
**index** | **int** |  | [optional] 
**embedding** | **List[float]** |  | [optional] 

## Example

```python
from quantcdn.models.oai_embeddings200_response_data_inner import OaiEmbeddings200ResponseDataInner

# TODO update the JSON string below
json = "{}"
# create an instance of OaiEmbeddings200ResponseDataInner from a JSON string
oai_embeddings200_response_data_inner_instance = OaiEmbeddings200ResponseDataInner.from_json(json)
# print the JSON string representation of the object
print(OaiEmbeddings200ResponseDataInner.to_json())

# convert the object into a dict
oai_embeddings200_response_data_inner_dict = oai_embeddings200_response_data_inner_instance.to_dict()
# create an instance of OaiEmbeddings200ResponseDataInner from a dict
oai_embeddings200_response_data_inner_from_dict = OaiEmbeddings200ResponseDataInner.from_dict(oai_embeddings200_response_data_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


