# AiSearchSearchRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**query** | **str** |  | 
**limit** | **int** |  | [optional] 
**min_score** | **float** |  | [optional] 

## Example

```python
from quantcdn.models.ai_search_search_request import AiSearchSearchRequest

# TODO update the JSON string below
json = "{}"
# create an instance of AiSearchSearchRequest from a JSON string
ai_search_search_request_instance = AiSearchSearchRequest.from_json(json)
# print the JSON string representation of the object
print(AiSearchSearchRequest.to_json())

# convert the object into a dict
ai_search_search_request_dict = ai_search_search_request_instance.to_dict()
# create an instance of AiSearchSearchRequest from a dict
ai_search_search_request_from_dict = AiSearchSearchRequest.from_dict(ai_search_search_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


