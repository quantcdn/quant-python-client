# ListMcpServers200ResponseServersInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**server_name** | **str** |  | [optional] 
**display_name** | **str** |  | [optional] 
**url** | **str** | MCP gateway URL | [optional] 
**enabled** | **bool** |  | [optional] 
**tool_allowlist** | **List[str]** |  | [optional] 

## Example

```python
from quantcdn.models.list_mcp_servers200_response_servers_inner import ListMcpServers200ResponseServersInner

# TODO update the JSON string below
json = "{}"
# create an instance of ListMcpServers200ResponseServersInner from a JSON string
list_mcp_servers200_response_servers_inner_instance = ListMcpServers200ResponseServersInner.from_json(json)
# print the JSON string representation of the object
print(ListMcpServers200ResponseServersInner.to_json())

# convert the object into a dict
list_mcp_servers200_response_servers_inner_dict = list_mcp_servers200_response_servers_inner_instance.to_dict()
# create an instance of ListMcpServers200ResponseServersInner from a dict
list_mcp_servers200_response_servers_inner_from_dict = ListMcpServers200ResponseServersInner.from_dict(list_mcp_servers200_response_servers_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


