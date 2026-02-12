# quantcdn.CDNMetricsApi

All URIs are relative to *https://dashboard.quantcdn.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_daily_metrics**](CDNMetricsApi.md#get_daily_metrics) | **GET** /v2/organizations/{organization}/projects/{project}/metrics/daily | Get daily metrics
[**get_hourly_metrics**](CDNMetricsApi.md#get_hourly_metrics) | **GET** /v2/organizations/{organization}/projects/{project}/metrics/hourly | Get hourly metrics
[**get_monthly_metrics**](CDNMetricsApi.md#get_monthly_metrics) | **GET** /v2/organizations/{organization}/projects/{project}/metrics/monthly | Get monthly metrics


# **get_daily_metrics**
> V2MetricsResponse get_daily_metrics(organization, project, domain=domain, metrics=metrics, timestamp_format=timestamp_format)

Get daily metrics

Returns the last 30 days of daily metrics data

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_metrics_response import V2MetricsResponse
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
    api_instance = quantcdn.CDNMetricsApi(api_client)
    organization = 'organization_example' # str | Organization identifier
    project = 'project_example' # str | Project identifier
    domain = 'domain_example' # str | Filter by domain ID or domain name (optional)
    metrics = ['metrics_example'] # List[str] | Metrics to return (default: hits, bytes) (optional)
    timestamp_format = iso8601 # str | Timestamp format in response (optional) (default to iso8601)

    try:
        # Get daily metrics
        api_response = api_instance.get_daily_metrics(organization, project, domain=domain, metrics=metrics, timestamp_format=timestamp_format)
        print("The response of CDNMetricsApi->get_daily_metrics:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CDNMetricsApi->get_daily_metrics: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **domain** | **str**| Filter by domain ID or domain name | [optional] 
 **metrics** | [**List[str]**](str.md)| Metrics to return (default: hits, bytes) | [optional] 
 **timestamp_format** | **str**| Timestamp format in response | [optional] [default to iso8601]

### Return type

[**V2MetricsResponse**](V2MetricsResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Daily metrics data |  -  |
**400** | Invalid metric requested |  -  |
**404** | No domains found or domain not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_hourly_metrics**
> V2MetricsResponse get_hourly_metrics(organization, project, domain=domain, metrics=metrics, timestamp_format=timestamp_format)

Get hourly metrics

Returns the last hour of minute-by-minute metrics data

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_metrics_response import V2MetricsResponse
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
    api_instance = quantcdn.CDNMetricsApi(api_client)
    organization = 'organization_example' # str | Organization identifier
    project = 'project_example' # str | Project identifier
    domain = 'domain_example' # str | Filter by domain ID or domain name (optional)
    metrics = ['metrics_example'] # List[str] | Metrics to return (default: hits, bytes) (optional)
    timestamp_format = iso8601 # str | Timestamp format in response (optional) (default to iso8601)

    try:
        # Get hourly metrics
        api_response = api_instance.get_hourly_metrics(organization, project, domain=domain, metrics=metrics, timestamp_format=timestamp_format)
        print("The response of CDNMetricsApi->get_hourly_metrics:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CDNMetricsApi->get_hourly_metrics: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **domain** | **str**| Filter by domain ID or domain name | [optional] 
 **metrics** | [**List[str]**](str.md)| Metrics to return (default: hits, bytes) | [optional] 
 **timestamp_format** | **str**| Timestamp format in response | [optional] [default to iso8601]

### Return type

[**V2MetricsResponse**](V2MetricsResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Hourly metrics data |  -  |
**400** | Invalid metric requested |  -  |
**404** | No domains found or domain not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_monthly_metrics**
> V2MetricsResponse get_monthly_metrics(organization, project, domain=domain, metrics=metrics, timestamp_format=timestamp_format)

Get monthly metrics

Returns the last 12 months of monthly metrics data

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_metrics_response import V2MetricsResponse
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
    api_instance = quantcdn.CDNMetricsApi(api_client)
    organization = 'organization_example' # str | Organization identifier
    project = 'project_example' # str | Project identifier
    domain = 'domain_example' # str | Filter by domain ID or domain name (optional)
    metrics = ['metrics_example'] # List[str] | Metrics to return (default: hits, bytes) (optional)
    timestamp_format = iso8601 # str | Timestamp format in response (optional) (default to iso8601)

    try:
        # Get monthly metrics
        api_response = api_instance.get_monthly_metrics(organization, project, domain=domain, metrics=metrics, timestamp_format=timestamp_format)
        print("The response of CDNMetricsApi->get_monthly_metrics:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CDNMetricsApi->get_monthly_metrics: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **domain** | **str**| Filter by domain ID or domain name | [optional] 
 **metrics** | [**List[str]**](str.md)| Metrics to return (default: hits, bytes) | [optional] 
 **timestamp_format** | **str**| Timestamp format in response | [optional] [default to iso8601]

### Return type

[**V2MetricsResponse**](V2MetricsResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Monthly metrics data |  -  |
**400** | Invalid metric requested |  -  |
**404** | No domains found or domain not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

