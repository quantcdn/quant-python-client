# quantcdn.PurgeApi

All URIs are relative to *https://dashboard.quantcdn.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**purge_create**](PurgeApi.md#purge_create) | **POST** /api/v2/organizations/{organization}/projects/{project}/purge | Purge cache via URL or cache keys


# **purge_create**
> str purge_create(organization, project, purge_create_request)

Purge cache via URL or cache keys

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.purge_create_request import PurgeCreateRequest
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
    api_instance = quantcdn.PurgeApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    purge_create_request = quantcdn.PurgeCreateRequest() # PurgeCreateRequest | 

    try:
        # Purge cache via URL or cache keys
        api_response = api_instance.purge_create(organization, project, purge_create_request)
        print("The response of PurgeApi->purge_create:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PurgeApi->purge_create: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **purge_create_request** | [**PurgeCreateRequest**](PurgeCreateRequest.md)|  | 

### Return type

**str**

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

