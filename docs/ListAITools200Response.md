# ListAITools200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tools** | [**List[ListAITools200ResponseToolsInner]**](ListAITools200ResponseToolsInner.md) | Array of available tool specifications | 
**count** | **int** | Number of available tools | 

## Example

```python
from quantcdn.models.list_ai_tools200_response import ListAITools200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ListAITools200Response from a JSON string
list_ai_tools200_response_instance = ListAITools200Response.from_json(json)
# print the JSON string representation of the object
print(ListAITools200Response.to_json())

# convert the object into a dict
list_ai_tools200_response_dict = list_ai_tools200_response_instance.to_dict()
# create an instance of ListAITools200Response from a dict
list_ai_tools200_response_from_dict = ListAITools200Response.from_dict(list_ai_tools200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


