# quantcdn.HeadersApi

All URIs are relative to *https://dashboard.quantcdn.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**headers_create**](HeadersApi.md#headers_create) | **POST** /api/v2/organizations/{organization}/projects/{project}/custom-headers | Create or update custom headers
[**headers_delete**](HeadersApi.md#headers_delete) | **DELETE** /api/v2/organizations/{organization}/projects/{project}/custom-headers | Delete custom headers
[**headers_list**](HeadersApi.md#headers_list) | **GET** /api/v2/organizations/{organization}/projects/{project}/custom-headers | List custom headers for a project


# **headers_create**
> Dict[str, str] headers_create(organization, project, v2_custom_header_request)

Create or update custom headers

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_custom_header_request import V2CustomHeaderRequest
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
    api_instance = quantcdn.HeadersApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    v2_custom_header_request = quantcdn.V2CustomHeaderRequest() # V2CustomHeaderRequest | 

    try:
        # Create or update custom headers
        api_response = api_instance.headers_create(organization, project, v2_custom_header_request)
        print("The response of HeadersApi->headers_create:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling HeadersApi->headers_create: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **v2_custom_header_request** | [**V2CustomHeaderRequest**](V2CustomHeaderRequest.md)|  | 

### Return type

**Dict[str, str]**

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The request has succeeded. |  -  |
**400** | The server could not understand the request due to invalid syntax. |  -  |
**403** | Access is forbidden. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **headers_delete**
> headers_delete(organization, project, v2_custom_header_request)

Delete custom headers

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_custom_header_request import V2CustomHeaderRequest
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
    api_instance = quantcdn.HeadersApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    v2_custom_header_request = quantcdn.V2CustomHeaderRequest() # V2CustomHeaderRequest | 

    try:
        # Delete custom headers
        api_instance.headers_delete(organization, project, v2_custom_header_request)
    except Exception as e:
        print("Exception when calling HeadersApi->headers_delete: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **v2_custom_header_request** | [**V2CustomHeaderRequest**](V2CustomHeaderRequest.md)|  | 

### Return type

void (empty response body)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | The headers have been deleted. |  -  |
**400** | The server could not understand the request due to invalid syntax. |  -  |
**403** | Access is forbidden. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **headers_list**
> Dict[str, str] headers_list(organization, project)

List custom headers for a project

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
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
    api_instance = quantcdn.HeadersApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier

    try:
        # List custom headers for a project
        api_response = api_instance.headers_list(organization, project)
        print("The response of HeadersApi->headers_list:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling HeadersApi->headers_list: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 

### Return type

**Dict[str, str]**

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The request has succeeded. |  -  |
**400** | The server could not understand the request due to invalid syntax. |  -  |
**403** | Access is forbidden. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

