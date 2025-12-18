# CreateAISession201Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**session_id** | **str** |  | [optional] 
**status** | **str** |  | [optional] 
**expires_at** | **datetime** |  | [optional] 
**created_at** | **datetime** |  | [optional] 

## Example

```python
from quantcdn.models.create_ai_session201_response import CreateAISession201Response

# TODO update the JSON string below
json = "{}"
# create an instance of CreateAISession201Response from a JSON string
create_ai_session201_response_instance = CreateAISession201Response.from_json(json)
# print the JSON string representation of the object
print(CreateAISession201Response.to_json())

# convert the object into a dict
create_ai_session201_response_dict = create_ai_session201_response_instance.to_dict()
# create an instance of CreateAISession201Response from a dict
create_ai_session201_response_from_dict = CreateAISession201Response.from_dict(create_ai_session201_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


