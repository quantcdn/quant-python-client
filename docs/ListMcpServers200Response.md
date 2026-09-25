# ListMcpServers200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**gateway_base_url** | **str** | Origin of the MCP gateway host (scheme://host[:port]) — clients treat gateway URLs on this origin as bearer-authenticated with the end user&#39;s Quant token | [optional] 
**servers** | [**List[ListMcpServers200ResponseServersInner]**](ListMcpServers200ResponseServersInner.md) |  | [optional] 

## Example

```python
from quantcdn.models.list_mcp_servers200_response import ListMcpServers200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ListMcpServers200Response from a JSON string
list_mcp_servers200_response_instance = ListMcpServers200Response.from_json(json)
# print the JSON string representation of the object
print(ListMcpServers200Response.to_json())

# convert the object into a dict
list_mcp_servers200_response_dict = list_mcp_servers200_response_instance.to_dict()
# create an instance of ListMcpServers200Response from a dict
list_mcp_servers200_response_from_dict = ListMcpServers200Response.from_dict(list_mcp_servers200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


