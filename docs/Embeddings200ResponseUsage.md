# Embeddings200ResponseUsage


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**input_tokens** | **int** | Number of tokens in input text(s) | 
**total_tokens** | **int** | Total tokens (same as inputTokens for embeddings) | 

## Example

```python
from quantcdn.models.embeddings200_response_usage import Embeddings200ResponseUsage

# TODO update the JSON string below
json = "{}"
# create an instance of Embeddings200ResponseUsage from a JSON string
embeddings200_response_usage_instance = Embeddings200ResponseUsage.from_json(json)
# print the JSON string representation of the object
print(Embeddings200ResponseUsage.to_json())

# convert the object into a dict
embeddings200_response_usage_dict = embeddings200_response_usage_instance.to_dict()
# create an instance of Embeddings200ResponseUsage from a dict
embeddings200_response_usage_from_dict = Embeddings200ResponseUsage.from_dict(embeddings200_response_usage_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


