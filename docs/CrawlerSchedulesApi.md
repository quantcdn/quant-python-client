# quantcdn.CrawlerSchedulesApi

All URIs are relative to *https://dashboard.quantcdn.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**crawler_schedules_add**](CrawlerSchedulesApi.md#crawler_schedules_add) | **POST** /api/v2/organizations/{organization}/projects/{project}/crawlers/{crawler}/schedules | Add a new schedule
[**crawler_schedules_delete**](CrawlerSchedulesApi.md#crawler_schedules_delete) | **DELETE** /api/v2/organizations/{organization}/projects/{project}/crawlers/{crawler}/schedules/{crawler_schedule} | Delete a schedule
[**crawler_schedules_edit**](CrawlerSchedulesApi.md#crawler_schedules_edit) | **PATCH** /api/v2/organizations/{organization}/projects/{project}/crawlers/{crawler}/schedules/{crawler_schedule} | Edit a schedule
[**crawler_schedules_list**](CrawlerSchedulesApi.md#crawler_schedules_list) | **GET** /api/v2/organizations/{organization}/projects/{project}/crawlers/{crawler}/schedules | List schedules for a crawler
[**crawler_schedules_show**](CrawlerSchedulesApi.md#crawler_schedules_show) | **GET** /api/v2/organizations/{organization}/projects/{project}/crawlers/{crawler}/schedules/{crawler_schedule} | Show a specific schedule


# **crawler_schedules_add**
> V2CrawlerSchedule crawler_schedules_add(organization, project, crawler, v2_crawler_schedule_request)

Add a new schedule

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_crawler_schedule import V2CrawlerSchedule
from quantcdn.models.v2_crawler_schedule_request import V2CrawlerScheduleRequest
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
    api_instance = quantcdn.CrawlerSchedulesApi(api_client)
    organization = 'organization_example' # str | Organization identifier
    project = 'project_example' # str | Project identifier
    crawler = 'crawler_example' # str | Crawler identifier
    v2_crawler_schedule_request = quantcdn.V2CrawlerScheduleRequest() # V2CrawlerScheduleRequest | 

    try:
        # Add a new schedule
        api_response = api_instance.crawler_schedules_add(organization, project, crawler, v2_crawler_schedule_request)
        print("The response of CrawlerSchedulesApi->crawler_schedules_add:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CrawlerSchedulesApi->crawler_schedules_add: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **crawler** | **str**| Crawler identifier | 
 **v2_crawler_schedule_request** | [**V2CrawlerScheduleRequest**](V2CrawlerScheduleRequest.md)|  | 

### Return type

[**V2CrawlerSchedule**](V2CrawlerSchedule.md)

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

# **crawler_schedules_delete**
> crawler_schedules_delete(organization, project, crawler, crawler_schedule)

Delete a schedule

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
    api_instance = quantcdn.CrawlerSchedulesApi(api_client)
    organization = 'organization_example' # str | Organization identifier
    project = 'project_example' # str | Project identifier
    crawler = 'crawler_example' # str | Crawler identifier
    crawler_schedule = 'crawler_schedule_example' # str | Crawler schedule identifier

    try:
        # Delete a schedule
        api_instance.crawler_schedules_delete(organization, project, crawler, crawler_schedule)
    except Exception as e:
        print("Exception when calling CrawlerSchedulesApi->crawler_schedules_delete: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **crawler** | **str**| Crawler identifier | 
 **crawler_schedule** | **str**| Crawler schedule identifier | 

### Return type

void (empty response body)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | The crawler schedule has been deleted. |  -  |
**400** | The server could not understand the request due to invalid syntax. |  -  |
**403** | Access is forbidden. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **crawler_schedules_edit**
> V2CrawlerSchedule crawler_schedules_edit(organization, project, crawler, crawler_schedule, v2_crawler_schedule_request)

Edit a schedule

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_crawler_schedule import V2CrawlerSchedule
from quantcdn.models.v2_crawler_schedule_request import V2CrawlerScheduleRequest
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
    api_instance = quantcdn.CrawlerSchedulesApi(api_client)
    organization = 'organization_example' # str | Organization identifier
    project = 'project_example' # str | Project identifier
    crawler = 'crawler_example' # str | Crawler identifier
    crawler_schedule = 'crawler_schedule_example' # str | Crawler schedule identifier
    v2_crawler_schedule_request = quantcdn.V2CrawlerScheduleRequest() # V2CrawlerScheduleRequest | 

    try:
        # Edit a schedule
        api_response = api_instance.crawler_schedules_edit(organization, project, crawler, crawler_schedule, v2_crawler_schedule_request)
        print("The response of CrawlerSchedulesApi->crawler_schedules_edit:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CrawlerSchedulesApi->crawler_schedules_edit: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **crawler** | **str**| Crawler identifier | 
 **crawler_schedule** | **str**| Crawler schedule identifier | 
 **v2_crawler_schedule_request** | [**V2CrawlerScheduleRequest**](V2CrawlerScheduleRequest.md)|  | 

### Return type

[**V2CrawlerSchedule**](V2CrawlerSchedule.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The crawler schedule. |  -  |
**400** | The server could not understand the request due to invalid syntax. |  -  |
**403** | Access is forbidden. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **crawler_schedules_list**
> List[V2CrawlerSchedule] crawler_schedules_list(organization, project, crawler)

List schedules for a crawler

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_crawler_schedule import V2CrawlerSchedule
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
    api_instance = quantcdn.CrawlerSchedulesApi(api_client)
    organization = 'organization_example' # str | 
    project = 'project_example' # str | 
    crawler = 'crawler_example' # str | 

    try:
        # List schedules for a crawler
        api_response = api_instance.crawler_schedules_list(organization, project, crawler)
        print("The response of CrawlerSchedulesApi->crawler_schedules_list:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CrawlerSchedulesApi->crawler_schedules_list: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**|  | 
 **project** | **str**|  | 
 **crawler** | **str**|  | 

### Return type

[**List[V2CrawlerSchedule]**](V2CrawlerSchedule.md)

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

# **crawler_schedules_show**
> V2CrawlerSchedule crawler_schedules_show(organization, project, crawler, crawler_schedule)

Show a specific schedule

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_crawler_schedule import V2CrawlerSchedule
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
    api_instance = quantcdn.CrawlerSchedulesApi(api_client)
    organization = 'organization_example' # str | Organization identifier
    project = 'project_example' # str | Project identifier
    crawler = 'crawler_example' # str | Crawler identifier
    crawler_schedule = 'crawler_schedule_example' # str | Crawler schedule identifier

    try:
        # Show a specific schedule
        api_response = api_instance.crawler_schedules_show(organization, project, crawler, crawler_schedule)
        print("The response of CrawlerSchedulesApi->crawler_schedules_show:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CrawlerSchedulesApi->crawler_schedules_show: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **crawler** | **str**| Crawler identifier | 
 **crawler_schedule** | **str**| Crawler schedule identifier | 

### Return type

[**V2CrawlerSchedule**](V2CrawlerSchedule.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The crawler schedule. |  -  |
**400** | The server could not understand the request due to invalid syntax. |  -  |
**403** | Access is forbidden. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

