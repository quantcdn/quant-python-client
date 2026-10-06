# quantcdn.OpenAICompatibilityApi

All URIs are relative to *https://dashboard.quantcdn.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**oai_chat_completions**](OpenAICompatibilityApi.md#oai_chat_completions) | **POST** /oai/v1/chat/completions | Create a chat completion (OpenAI-compatible)
[**oai_embeddings**](OpenAICompatibilityApi.md#oai_embeddings) | **POST** /oai/v1/embeddings | Create embeddings (OpenAI-compatible)
[**oai_get_model**](OpenAICompatibilityApi.md#oai_get_model) | **GET** /oai/v1/models/{model} | Retrieve a model (OpenAI-compatible)
[**oai_list_models**](OpenAICompatibilityApi.md#oai_list_models) | **GET** /oai/v1/models | List available models (OpenAI-compatible)


# **oai_chat_completions**
> OaiChatCompletions200Response oai_chat_completions(oai_chat_completions_request)

Create a chat completion (OpenAI-compatible)

Drop-in replacement for OpenAI's POST /v1/chat/completions. Point any OpenAI SDK at base_url=https://<host>/oai/v1 and use a Quant API token (qc_...) as the api_key. Set `stream: true` to receive Server-Sent Events (chat.completion.chunk objects terminated by `data: [DONE]`); otherwise a single chat.completion object is returned. Supports tool/function calling and the standard tool_choice modes.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.oai_chat_completions200_response import OaiChatCompletions200Response
from quantcdn.models.oai_chat_completions_request import OaiChatCompletionsRequest
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
    api_instance = quantcdn.OpenAICompatibilityApi(api_client)
    oai_chat_completions_request = quantcdn.OaiChatCompletionsRequest() # OaiChatCompletionsRequest | 

    try:
        # Create a chat completion (OpenAI-compatible)
        api_response = api_instance.oai_chat_completions(oai_chat_completions_request)
        print("The response of OpenAICompatibilityApi->oai_chat_completions:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OpenAICompatibilityApi->oai_chat_completions: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **oai_chat_completions_request** | [**OaiChatCompletionsRequest**](OaiChatCompletionsRequest.md)|  | 

### Return type

[**OaiChatCompletions200Response**](OaiChatCompletions200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | A chat.completion object (or an SSE stream of chat.completion.chunk objects when stream&#x3D;true) |  -  |
**401** | Missing or invalid API key |  -  |
**403** | Token not scoped to an organisation, or org lacks AI access |  -  |
**422** | Invalid request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **oai_embeddings**
> OaiEmbeddings200Response oai_embeddings(oai_embeddings_request)

Create embeddings (OpenAI-compatible)

Drop-in replacement for OpenAI's POST /v1/embeddings. Accepts a single string or an array of strings in `input` and returns a list of embedding objects.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.oai_embeddings200_response import OaiEmbeddings200Response
from quantcdn.models.oai_embeddings_request import OaiEmbeddingsRequest
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
    api_instance = quantcdn.OpenAICompatibilityApi(api_client)
    oai_embeddings_request = quantcdn.OaiEmbeddingsRequest() # OaiEmbeddingsRequest | 

    try:
        # Create embeddings (OpenAI-compatible)
        api_response = api_instance.oai_embeddings(oai_embeddings_request)
        print("The response of OpenAICompatibilityApi->oai_embeddings:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OpenAICompatibilityApi->oai_embeddings: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **oai_embeddings_request** | [**OaiEmbeddingsRequest**](OaiEmbeddingsRequest.md)|  | 

### Return type

[**OaiEmbeddings200Response**](OaiEmbeddings200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | A list of embedding objects |  -  |
**401** | Missing or invalid API key |  -  |
**403** | Token not scoped to an organisation, or org lacks AI access |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **oai_get_model**
> OaiGetModel200Response oai_get_model(model)

Retrieve a model (OpenAI-compatible)

Drop-in replacement for OpenAI's GET /v1/models/{model}.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.oai_get_model200_response import OaiGetModel200Response
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
    api_instance = quantcdn.OpenAICompatibilityApi(api_client)
    model = 'amazon.nova-micro-v1:0' # str | 

    try:
        # Retrieve a model (OpenAI-compatible)
        api_response = api_instance.oai_get_model(model)
        print("The response of OpenAICompatibilityApi->oai_get_model:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OpenAICompatibilityApi->oai_get_model: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **model** | **str**|  | 

### Return type

[**OaiGetModel200Response**](OaiGetModel200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | A model object |  -  |
**401** | Missing or invalid API key |  -  |
**404** | Model not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **oai_list_models**
> OaiListModels200Response oai_list_models()

List available models (OpenAI-compatible)

Drop-in replacement for OpenAI's GET /v1/models. Returns the model ids available to the organisation; pass one of these ids as `model` in chat/embeddings requests.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.oai_list_models200_response import OaiListModels200Response
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
    api_instance = quantcdn.OpenAICompatibilityApi(api_client)

    try:
        # List available models (OpenAI-compatible)
        api_response = api_instance.oai_list_models()
        print("The response of OpenAICompatibilityApi->oai_list_models:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OpenAICompatibilityApi->oai_list_models: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**OaiListModels200Response**](OaiListModels200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | A list of model objects |  -  |
**401** | Missing or invalid API key |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

