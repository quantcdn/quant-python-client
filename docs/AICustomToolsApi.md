# quantcdn.AICustomToolsApi

All URIs are relative to *https://dashboard.quantcdn.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_custom_tool**](AICustomToolsApi.md#create_custom_tool) | **POST** /api/v3/organizations/{organisation}/ai/custom-tools | Register Custom Edge Function Tool
[**delete_custom_tool**](AICustomToolsApi.md#delete_custom_tool) | **DELETE** /api/v3/organizations/{organisation}/ai/custom-tools/{toolName} | Delete Custom Tool
[**list_custom_tools**](AICustomToolsApi.md#list_custom_tools) | **GET** /api/v3/organizations/{organisation}/ai/custom-tools | List Custom Tools


# **create_custom_tool**
> CreateCustomTool201Response create_custom_tool(organisation, create_custom_tool_request)

Register Custom Edge Function Tool

Registers a custom edge function as a tool that AI models can invoke. This enables customers to create their own tools backed by edge functions.
     *
     * **Edge Function Contract:**
     * - Edge functions must accept POST requests with JSON payload
     * - Expected request format: `{ 'toolName': '...', 'input': {...}, 'orgId': '...' }`
     * - Must return JSON response with either `result` or `error` field
     *
     * **Async Tools:**
     * Set `isAsync: true` for operations >5 seconds. The edge function should return `{ executionId: '...' }` and the AI will poll for completion.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.create_custom_tool201_response import CreateCustomTool201Response
from quantcdn.models.create_custom_tool_request import CreateCustomToolRequest
from quantcdn.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://dashboard.quantcdn.io
# See configuration.py for a list of all supported configuration parameters.
configuration = quantcdn.Configuration(
    host = "https://dashboard.quantcdn.io"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization (JWT): BearerAuth
configuration = quantcdn.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with quantcdn.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = quantcdn.AICustomToolsApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    create_custom_tool_request = quantcdn.CreateCustomToolRequest() # CreateCustomToolRequest | 

    try:
        # Register Custom Edge Function Tool
        api_response = api_instance.create_custom_tool(organisation, create_custom_tool_request)
        print("The response of AICustomToolsApi->create_custom_tool:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AICustomToolsApi->create_custom_tool: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **create_custom_tool_request** | [**CreateCustomToolRequest**](CreateCustomToolRequest.md)|  | 

### Return type

[**CreateCustomTool201Response**](CreateCustomTool201Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Custom tool registered successfully |  -  |
**400** | Invalid request parameters |  -  |
**403** | Access denied |  -  |
**409** | Tool with this name already exists |  -  |
**500** | Failed to register custom tool |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_custom_tool**
> DeleteCustomTool200Response delete_custom_tool(organisation, tool_name)

Delete Custom Tool

Deletes a custom tool registration. The underlying edge function is not affected.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.delete_custom_tool200_response import DeleteCustomTool200Response
from quantcdn.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://dashboard.quantcdn.io
# See configuration.py for a list of all supported configuration parameters.
configuration = quantcdn.Configuration(
    host = "https://dashboard.quantcdn.io"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization (JWT): BearerAuth
configuration = quantcdn.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with quantcdn.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = quantcdn.AICustomToolsApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    tool_name = 'tool_name_example' # str | The tool name to delete

    try:
        # Delete Custom Tool
        api_response = api_instance.delete_custom_tool(organisation, tool_name)
        print("The response of AICustomToolsApi->delete_custom_tool:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AICustomToolsApi->delete_custom_tool: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **tool_name** | **str**| The tool name to delete | 

### Return type

[**DeleteCustomTool200Response**](DeleteCustomTool200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Custom tool deleted successfully |  -  |
**403** | Access denied |  -  |
**404** | Tool not found |  -  |
**500** | Failed to delete custom tool |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_custom_tools**
> ListCustomTools200Response list_custom_tools(organisation)

List Custom Tools

Lists all registered custom edge function tools for an organization.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.list_custom_tools200_response import ListCustomTools200Response
from quantcdn.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://dashboard.quantcdn.io
# See configuration.py for a list of all supported configuration parameters.
configuration = quantcdn.Configuration(
    host = "https://dashboard.quantcdn.io"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization (JWT): BearerAuth
configuration = quantcdn.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with quantcdn.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = quantcdn.AICustomToolsApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID

    try:
        # List Custom Tools
        api_response = api_instance.list_custom_tools(organisation)
        print("The response of AICustomToolsApi->list_custom_tools:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AICustomToolsApi->list_custom_tools: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 

### Return type

[**ListCustomTools200Response**](ListCustomTools200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Custom tools retrieved successfully |  -  |
**403** | Access denied |  -  |
**500** | Failed to retrieve custom tools |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

