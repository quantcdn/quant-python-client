# quantcdn.AIApi

All URIs are relative to *https://dashboard.quantcdn.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_ai_usage_stats**](AIApi.md#get_ai_usage_stats) | **GET** /api/v3/organizations/{organisation}/ai/usage | Organisation AI usage breakdown (subscription page parity)


# **get_ai_usage_stats**
> get_ai_usage_stats(organisation, month=month, group_by=group_by, include=include, user_id=user_id, token_id=token_id)

Organisation AI usage breakdown (subscription page parity)

AI usage from the subscription page's source (cloud-api monthly-usage). Parameterized by month, groupBy (model|user|token) and optional daily series. NOTE: as of API 4.19.0 this endpoint requires the update_subscription permission + subscription:read scope (previously use_ai_services + ai:use). For per-caller spend use /ai/usage/me.

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
    api_instance = quantcdn.AIApi(api_client)
    organisation = 'organisation_example' # str | 
    month = 'month_example' # str | YYYY-MM, defaults to current month (optional)
    group_by = model # str |  (optional) (default to model)
    include = 'include_example' # str | Set to 'daily' to append a 30-day series (optional)
    user_id = 'user_id_example' # str | Scope the daily series to a user (optional)
    token_id = 'token_id_example' # str | Scope the daily series to a token (optional)

    try:
        # Organisation AI usage breakdown (subscription page parity)
        api_instance.get_ai_usage_stats(organisation, month=month, group_by=group_by, include=include, user_id=user_id, token_id=token_id)
    except Exception as e:
        print("Exception when calling AIApi->get_ai_usage_stats: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**|  | 
 **month** | **str**| YYYY-MM, defaults to current month | [optional] 
 **group_by** | **str**|  | [optional] [default to model]
 **include** | **str**| Set to &#39;daily&#39; to append a 30-day series | [optional] 
 **user_id** | **str**| Scope the daily series to a user | [optional] 
 **token_id** | **str**| Scope the daily series to a token | [optional] 

### Return type

void (empty response body)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Usage breakdown |  -  |
**403** | Missing update_subscription permission or subscription:read scope |  -  |
**422** | Invalid groupBy |  -  |
**500** | Failed to fetch usage data |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

