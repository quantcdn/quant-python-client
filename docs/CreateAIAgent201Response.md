# CreateAIAgent201Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**agent** | **object** |  | [optional] 
**message** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.create_ai_agent201_response import CreateAIAgent201Response

# TODO update the JSON string below
json = "{}"
# create an instance of CreateAIAgent201Response from a JSON string
create_ai_agent201_response_instance = CreateAIAgent201Response.from_json(json)
# print the JSON string representation of the object
print(CreateAIAgent201Response.to_json())

# convert the object into a dict
create_ai_agent201_response_dict = create_ai_agent201_response_instance.to_dict()
# create an instance of CreateAIAgent201Response from a dict
create_ai_agent201_response_from_dict = CreateAIAgent201Response.from_dict(create_ai_agent201_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


