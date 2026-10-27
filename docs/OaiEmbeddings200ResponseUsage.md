# OaiEmbeddings200ResponseUsage


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**prompt_tokens** | **int** |  | [optional] 
**total_tokens** | **int** |  | [optional] 

## Example

```python
from quantcdn.models.oai_embeddings200_response_usage import OaiEmbeddings200ResponseUsage

# TODO update the JSON string below
json = "{}"
# create an instance of OaiEmbeddings200ResponseUsage from a JSON string
oai_embeddings200_response_usage_instance = OaiEmbeddings200ResponseUsage.from_json(json)
# print the JSON string representation of the object
print(OaiEmbeddings200ResponseUsage.to_json())

# convert the object into a dict
oai_embeddings200_response_usage_dict = oai_embeddings200_response_usage_instance.to_dict()
# create an instance of OaiEmbeddings200ResponseUsage from a dict
oai_embeddings200_response_usage_from_dict = OaiEmbeddings200ResponseUsage.from_dict(oai_embeddings200_response_usage_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


