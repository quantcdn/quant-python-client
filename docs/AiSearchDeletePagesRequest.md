# AiSearchDeletePagesRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**urls** | **List[str]** |  | [optional] 
**patterns** | **List[str]** |  | [optional] 

## Example

```python
from quantcdn.models.ai_search_delete_pages_request import AiSearchDeletePagesRequest

# TODO update the JSON string below
json = "{}"
# create an instance of AiSearchDeletePagesRequest from a JSON string
ai_search_delete_pages_request_instance = AiSearchDeletePagesRequest.from_json(json)
# print the JSON string representation of the object
print(AiSearchDeletePagesRequest.to_json())

# convert the object into a dict
ai_search_delete_pages_request_dict = ai_search_delete_pages_request_instance.to_dict()
# create an instance of AiSearchDeletePagesRequest from a dict
ai_search_delete_pages_request_from_dict = AiSearchDeletePagesRequest.from_dict(ai_search_delete_pages_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


