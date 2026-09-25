# quantcdn.TokensApi

All URIs are relative to *https://dashboard.quantcdn.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**tokens_create**](TokensApi.md#tokens_create) | **POST** /api/v2/organizations/{organization}/tokens | Create a new API token scoped to this organization
[**tokens_delete**](TokensApi.md#tokens_delete) | **DELETE** /api/v2/organizations/{organization}/tokens/{token_id} | Revoke an API token
[**tokens_list**](TokensApi.md#tokens_list) | **GET** /api/v2/organizations/{organization}/tokens | List API tokens scoped to this organization


# **tokens_create**
> TokensCreate201Response tokens_create(organization, tokens_create_request)

Create a new API token scoped to this organization

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.tokens_create201_response import TokensCreate201Response
from quantcdn.models.tokens_create_request import TokensCreateRequest
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
    api_instance = quantcdn.TokensApi(api_client)
    organization = 'test-org' # str | Organization identifier
    tokens_create_request = quantcdn.TokensCreateRequest() # TokensCreateRequest | 

    try:
        # Create a new API token scoped to this organization
        api_response = api_instance.tokens_create(organization, tokens_create_request)
        print("The response of TokensApi->tokens_create:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TokensApi->tokens_create: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **tokens_create_request** | [**TokensCreateRequest**](TokensCreateRequest.md)|  | 

### Return type

[**TokensCreate201Response**](TokensCreate201Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Token created. The plain token is returned once and cannot be retrieved again. |  -  |
**400** | Bad request. |  -  |
**403** | Access is forbidden. |  -  |
**422** | Validation error. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tokens_delete**
> TokensDelete200Response tokens_delete(organization, token_id)

Revoke an API token

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.tokens_delete200_response import TokensDelete200Response
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
    api_instance = quantcdn.TokensApi(api_client)
    organization = 'test-org' # str | Organization identifier
    token_id = 42 # int | Token ID to revoke

    try:
        # Revoke an API token
        api_response = api_instance.tokens_delete(organization, token_id)
        print("The response of TokensApi->tokens_delete:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TokensApi->tokens_delete: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **token_id** | **int**| Token ID to revoke | 

### Return type

[**TokensDelete200Response**](TokensDelete200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Token revoked successfully. |  -  |
**403** | Access is forbidden. |  -  |
**404** | Token not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tokens_list**
> List[TokensList200ResponseInner] tokens_list(organization)

List API tokens scoped to this organization

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.tokens_list200_response_inner import TokensList200ResponseInner
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
    api_instance = quantcdn.TokensApi(api_client)
    organization = 'test-org' # str | Organization identifier

    try:
        # List API tokens scoped to this organization
        api_response = api_instance.tokens_list(organization)
        print("The response of TokensApi->tokens_list:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TokensApi->tokens_list: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 

### Return type

[**List[TokensList200ResponseInner]**](TokensList200ResponseInner.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The request has succeeded. |  -  |
**403** | Access is forbidden. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

