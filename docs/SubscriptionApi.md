# quantcdn.SubscriptionApi

All URIs are relative to *https://dashboard.quantcdn.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_subscription_cloud_usage**](SubscriptionApi.md#get_subscription_cloud_usage) | **GET** /api/v3/organizations/{organisation}/subscription/cloud-usage | Cloud-app cost breakdown for the subscription page


# **get_subscription_cloud_usage**
> get_subscription_cloud_usage(organisation, month=month)

Cloud-app cost breakdown for the subscription page

Per-project compute/database/storage cost breakdown with spot discount, for the requested month and the month before it. Mirrors the subscription page's Cloud Apps card.

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
    api_instance = quantcdn.SubscriptionApi(api_client)
    organisation = 'organisation_example' # str | 
    month = 'month_example' # str | YYYY-MM, defaults to current month (optional)

    try:
        # Cloud-app cost breakdown for the subscription page
        api_instance.get_subscription_cloud_usage(organisation, month=month)
    except Exception as e:
        print("Exception when calling SubscriptionApi->get_subscription_cloud_usage: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**|  | 
 **month** | **str**| YYYY-MM, defaults to current month | [optional] 

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
**200** | Usage envelope |  -  |
**403** | Missing update_subscription permission or subscription:read scope |  -  |
**500** | Failed to fetch usage data |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

