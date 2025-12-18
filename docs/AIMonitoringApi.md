# quantcdn.AIMonitoringApi

All URIs are relative to *https://dashboard.quantcdn.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_ai_usage_stats**](AIMonitoringApi.md#get_ai_usage_stats) | **GET** /api/v3/organizations/{organisation}/ai/usage | Get AI usage statistics


# **get_ai_usage_stats**
> GetAIUsageStats200Response get_ai_usage_stats(organisation, month=month)

Get AI usage statistics

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.get_ai_usage_stats200_response import GetAIUsageStats200Response
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
    api_instance = quantcdn.AIMonitoringApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    month = '2025-10' # str | Month to retrieve statistics for (YYYY-MM format) (optional)

    try:
        # Get AI usage statistics
        api_response = api_instance.get_ai_usage_stats(organisation, month=month)
        print("The response of AIMonitoringApi->get_ai_usage_stats:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIMonitoringApi->get_ai_usage_stats: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **month** | **str**| Month to retrieve statistics for (YYYY-MM format) | [optional] 

### Return type

[**GetAIUsageStats200Response**](GetAIUsageStats200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Usage statistics |  -  |
**500** | Failed to fetch usage statistics |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

