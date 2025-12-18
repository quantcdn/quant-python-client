# ChatInferenceRequestToolConfigToolsInnerToolSpec


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**input_schema** | [**ChatInferenceRequestToolConfigToolsInnerToolSpecInputSchema**](ChatInferenceRequestToolConfigToolsInnerToolSpecInputSchema.md) |  | [optional] 

## Example

```python
from quantcdn.models.chat_inference_request_tool_config_tools_inner_tool_spec import ChatInferenceRequestToolConfigToolsInnerToolSpec

# TODO update the JSON string below
json = "{}"
# create an instance of ChatInferenceRequestToolConfigToolsInnerToolSpec from a JSON string
chat_inference_request_tool_config_tools_inner_tool_spec_instance = ChatInferenceRequestToolConfigToolsInnerToolSpec.from_json(json)
# print the JSON string representation of the object
print(ChatInferenceRequestToolConfigToolsInnerToolSpec.to_json())

# convert the object into a dict
chat_inference_request_tool_config_tools_inner_tool_spec_dict = chat_inference_request_tool_config_tools_inner_tool_spec_instance.to_dict()
# create an instance of ChatInferenceRequestToolConfigToolsInnerToolSpec from a dict
chat_inference_request_tool_config_tools_inner_tool_spec_from_dict = ChatInferenceRequestToolConfigToolsInnerToolSpec.from_dict(chat_inference_request_tool_config_tools_inner_tool_spec_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


