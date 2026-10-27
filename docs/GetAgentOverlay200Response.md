# GetAgentOverlay200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**overlay** | [**GetAgentOverlay200ResponseOverlay**](GetAgentOverlay200ResponseOverlay.md) |  | [optional] 
**base** | [**GetAgentOverlay200ResponseBase**](GetAgentOverlay200ResponseBase.md) |  | [optional] 

## Example

```python
from quantcdn.models.get_agent_overlay200_response import GetAgentOverlay200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetAgentOverlay200Response from a JSON string
get_agent_overlay200_response_instance = GetAgentOverlay200Response.from_json(json)
# print the JSON string representation of the object
print(GetAgentOverlay200Response.to_json())

# convert the object into a dict
get_agent_overlay200_response_dict = get_agent_overlay200_response_instance.to_dict()
# create an instance of GetAgentOverlay200Response from a dict
get_agent_overlay200_response_from_dict = GetAgentOverlay200Response.from_dict(get_agent_overlay200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


