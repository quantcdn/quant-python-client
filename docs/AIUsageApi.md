# quantcdn.AIUsageApi

All URIs are relative to *https://dashboard.quantcdn.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_my_usage**](AIUsageApi.md#get_my_usage) | **GET** /api/v3/organizations/{organisation}/ai/usage/me | Get AI usage summary for the authenticated user


# **get_my_usage**
> GetMyUsage200Response get_my_usage(organisation)

Get AI usage summary for the authenticated user

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.get_my_usage200_response import GetMyUsage200Response
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
    api_instance = quantcdn.AIUsageApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID

    try:
        # Get AI usage summary for the authenticated user
        api_response = api_instance.get_my_usage(organisation)
        print("The response of AIUsageApi->get_my_usage:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIUsageApi->get_my_usage: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 

### Return type

[**GetMyUsage200Response**](GetMyUsage200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | User AI usage summary |  -  |
**401** | Cannot determine caller identity |  -  |
**500** | Failed to retrieve usage data |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

