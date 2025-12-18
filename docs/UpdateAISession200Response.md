# UpdateAISession200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**session_id** | **str** |  | [optional] 
**status** | **str** |  | [optional] 
**total_messages** | **int** |  | [optional] 
**total_tokens** | **int** |  | [optional] 
**updated_at** | **datetime** |  | [optional] 

## Example

```python
from quantcdn.models.update_ai_session200_response import UpdateAISession200Response

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateAISession200Response from a JSON string
update_ai_session200_response_instance = UpdateAISession200Response.from_json(json)
# print the JSON string representation of the object
print(UpdateAISession200Response.to_json())

# convert the object into a dict
update_ai_session200_response_dict = update_ai_session200_response_instance.to_dict()
# create an instance of UpdateAISession200Response from a dict
update_ai_session200_response_from_dict = UpdateAISession200Response.from_dict(update_ai_session200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


