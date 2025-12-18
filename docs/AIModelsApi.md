# quantcdn.AIModelsApi

All URIs are relative to *https://dashboard.quantcdn.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_ai_model**](AIModelsApi.md#get_ai_model) | **GET** /api/v3/organizations/{organisation}/ai/models/{modelId} | Get AI Model Details
[**list_ai_models**](AIModelsApi.md#list_ai_models) | **GET** /api/v3/organizations/{organisation}/ai/models | List available AI models for an organization


# **get_ai_model**
> GetAIModel200Response get_ai_model(organisation, model_id)

Get AI Model Details

Retrieves detailed information about a specific Bedrock model from the catalog.
     *
     * **Features:**
     * - Complete pricing breakdown (input/output per million tokens)
     * - Context window and output token limits
     * - Supported features (chat, vision, streaming, embeddings)
     * - Model availability and deprecation status
     * - Release date for version tracking
     *
     * **Example Model IDs:**
     * - `amazon.nova-lite-v1:0` - Default multimodal model
     * - `anthropic.claude-3-5-sonnet-20241022-v2:0` - Latest Claude
     * - `amazon.titan-embed-text-v2:0` - Latest embeddings

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.get_ai_model200_response import GetAIModel200Response
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
    api_instance = quantcdn.AIModelsApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    model_id = 'amazon.nova-lite-v1:0' # str | The model identifier (e.g., amazon.nova-lite-v1:0)

    try:
        # Get AI Model Details
        api_response = api_instance.get_ai_model(organisation, model_id)
        print("The response of AIModelsApi->get_ai_model:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIModelsApi->get_ai_model: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **model_id** | **str**| The model identifier (e.g., amazon.nova-lite-v1:0) | 

### Return type

[**GetAIModel200Response**](GetAIModel200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Model details retrieved successfully |  -  |
**404** | Model not found in catalog |  -  |
**500** | Failed to fetch model details |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_ai_models**
> ListAIModels200Response list_ai_models(organisation, feature=feature)

List available AI models for an organization

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.list_ai_models200_response import ListAIModels200Response
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
    api_instance = quantcdn.AIModelsApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    feature = all # str | Filter models by supported feature (optional) (default to all)

    try:
        # List available AI models for an organization
        api_response = api_instance.list_ai_models(organisation, feature=feature)
        print("The response of AIModelsApi->list_ai_models:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIModelsApi->list_ai_models: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **feature** | **str**| Filter models by supported feature | [optional] [default to all]

### Return type

[**ListAIModels200Response**](ListAIModels200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | List of available AI models |  -  |
**500** | Failed to fetch models |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

