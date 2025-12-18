# ExtendAISession200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**session_id** | **str** |  | [optional] 
**expires_at** | **datetime** |  | [optional] 
**message** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.extend_ai_session200_response import ExtendAISession200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ExtendAISession200Response from a JSON string
extend_ai_session200_response_instance = ExtendAISession200Response.from_json(json)
# print the JSON string representation of the object
print(ExtendAISession200Response.to_json())

# convert the object into a dict
extend_ai_session200_response_dict = extend_ai_session200_response_instance.to_dict()
# create an instance of ExtendAISession200Response from a dict
extend_ai_session200_response_from_dict = ExtendAISession200Response.from_dict(extend_ai_session200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


