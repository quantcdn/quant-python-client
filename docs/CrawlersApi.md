# quantcdn.CrawlersApi

All URIs are relative to *https://dashboard.quantcdn.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**crawlers_create**](CrawlersApi.md#crawlers_create) | **POST** /api/v2/organizations/{organization}/projects/{project}/crawlers | Create a new crawler
[**crawlers_delete**](CrawlersApi.md#crawlers_delete) | **DELETE** /api/v2/organizations/{organization}/projects/{project}/crawlers/{crawler} | Delete a crawler
[**crawlers_get_run_by_id**](CrawlersApi.md#crawlers_get_run_by_id) | **GET** /api/v2/organizations/{organization}/projects/{project}/crawlers/{crawler}/runs/{run_id} | Get a run by ID
[**crawlers_get_runs**](CrawlersApi.md#crawlers_get_runs) | **GET** /api/v2/organizations/{organization}/projects/{project}/crawlers/{crawler}/runs | Get all runs for a crawler
[**crawlers_list**](CrawlersApi.md#crawlers_list) | **GET** /api/v2/organizations/{organization}/projects/{project}/crawlers | List crawlers for the project
[**crawlers_read**](CrawlersApi.md#crawlers_read) | **GET** /api/v2/organizations/{organization}/projects/{project}/crawlers/{crawler} | Get details of a single crawler
[**crawlers_run**](CrawlersApi.md#crawlers_run) | **POST** /api/v2/organizations/{organization}/projects/{project}/crawlers/{crawler}/run | Run a crawler
[**crawlers_update**](CrawlersApi.md#crawlers_update) | **PATCH** /api/v2/organizations/{organization}/projects/{project}/crawlers/{crawler} | Update a crawler


# **crawlers_create**
> V2Crawler crawlers_create(organization, project, v2_crawler_request)

Create a new crawler

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_crawler import V2Crawler
from quantcdn.models.v2_crawler_request import V2CrawlerRequest
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
    api_instance = quantcdn.CrawlersApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    v2_crawler_request = quantcdn.V2CrawlerRequest() # V2CrawlerRequest | 

    try:
        # Create a new crawler
        api_response = api_instance.crawlers_create(organization, project, v2_crawler_request)
        print("The response of CrawlersApi->crawlers_create:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CrawlersApi->crawlers_create: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **v2_crawler_request** | [**V2CrawlerRequest**](V2CrawlerRequest.md)|  | 

### Return type

[**V2Crawler**](V2Crawler.md)

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

# **crawlers_delete**
> crawlers_delete(organization, project, crawler)

Delete a crawler

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
    api_instance = quantcdn.CrawlersApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    crawler = '00000000-0000-0000-0000-000000000000' # str | The UUID of the crawler

    try:
        # Delete a crawler
        api_instance.crawlers_delete(organization, project, crawler)
    except Exception as e:
        print("Exception when calling CrawlersApi->crawlers_delete: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **crawler** | **str**| The UUID of the crawler | 

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
**204** | The request has succeeded. |  -  |
**400** | The server could not understand the request due to invalid syntax. |  -  |
**403** | Access is forbidden. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **crawlers_get_run_by_id**
> V2CrawlerRun crawlers_get_run_by_id(organization, project, crawler, run_id)

Get a run by ID

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_crawler_run import V2CrawlerRun
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
    api_instance = quantcdn.CrawlersApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    crawler = '00000000-0000-0000-0000-000000000000' # str | Crawler identifier
    run_id = 1 # int | Run identifier

    try:
        # Get a run by ID
        api_response = api_instance.crawlers_get_run_by_id(organization, project, crawler, run_id)
        print("The response of CrawlersApi->crawlers_get_run_by_id:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CrawlersApi->crawlers_get_run_by_id: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **crawler** | **str**| Crawler identifier | 
 **run_id** | **int**| Run identifier | 

### Return type

[**V2CrawlerRun**](V2CrawlerRun.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The run |  -  |
**400** | The server could not understand the request due to invalid syntax. |  -  |
**403** | Access is forbidden. |  -  |
**404** | The resource was not found. |  -  |
**500** | An unexpected error occurred. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **crawlers_get_runs**
> List[V2CrawlerRun] crawlers_get_runs(organization, project, crawler)

Get all runs for a crawler

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_crawler_run import V2CrawlerRun
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
    api_instance = quantcdn.CrawlersApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    crawler = '00000000-0000-0000-0000-000000000000' # str | Crawler identifier

    try:
        # Get all runs for a crawler
        api_response = api_instance.crawlers_get_runs(organization, project, crawler)
        print("The response of CrawlersApi->crawlers_get_runs:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CrawlersApi->crawlers_get_runs: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **crawler** | **str**| Crawler identifier | 

### Return type

[**List[V2CrawlerRun]**](V2CrawlerRun.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The runs |  -  |
**400** | The server could not understand the request due to invalid syntax. |  -  |
**403** | Access is forbidden. |  -  |
**404** | The resource was not found. |  -  |
**500** | An unexpected error occurred. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **crawlers_list**
> crawlers_list(organization, project)

List crawlers for the project

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
    api_instance = quantcdn.CrawlersApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier

    try:
        # List crawlers for the project
        api_instance.crawlers_list(organization, project)
    except Exception as e:
        print("Exception when calling CrawlersApi->crawlers_list: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 

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
**400** | The server could not understand the request due to invalid syntax. |  -  |
**403** | Access is forbidden. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **crawlers_read**
> V2Crawler crawlers_read(organization, project, crawler)

Get details of a single crawler

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_crawler import V2Crawler
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
    api_instance = quantcdn.CrawlersApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    crawler = '00000000-0000-0000-0000-000000000000' # str | The UUID of the crawler

    try:
        # Get details of a single crawler
        api_response = api_instance.crawlers_read(organization, project, crawler)
        print("The response of CrawlersApi->crawlers_read:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CrawlersApi->crawlers_read: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **crawler** | **str**| The UUID of the crawler | 

### Return type

[**V2Crawler**](V2Crawler.md)

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

# **crawlers_run**
> CrawlersRun200Response crawlers_run(organization, project, crawler, crawlers_run_request)

Run a crawler

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.crawlers_run200_response import CrawlersRun200Response
from quantcdn.models.crawlers_run_request import CrawlersRunRequest
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
    api_instance = quantcdn.CrawlersApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    crawler = '00000000-0000-0000-0000-000000000000' # str | Crawler identifier
    crawlers_run_request = quantcdn.CrawlersRunRequest() # CrawlersRunRequest | 

    try:
        # Run a crawler
        api_response = api_instance.crawlers_run(organization, project, crawler, crawlers_run_request)
        print("The response of CrawlersApi->crawlers_run:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CrawlersApi->crawlers_run: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **crawler** | **str**| Crawler identifier | 
 **crawlers_run_request** | [**CrawlersRunRequest**](CrawlersRunRequest.md)|  | 

### Return type

[**CrawlersRun200Response**](CrawlersRun200Response.md)

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
**404** | The resource was not found. |  -  |
**500** | An unexpected error occurred. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **crawlers_update**
> V2Crawler crawlers_update(organization, project, crawler, v2_crawler_request)

Update a crawler

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_crawler import V2Crawler
from quantcdn.models.v2_crawler_request import V2CrawlerRequest
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
    api_instance = quantcdn.CrawlersApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    crawler = '00000000-0000-0000-0000-000000000000' # str | The UUID of the crawler
    v2_crawler_request = quantcdn.V2CrawlerRequest() # V2CrawlerRequest | 

    try:
        # Update a crawler
        api_response = api_instance.crawlers_update(organization, project, crawler, v2_crawler_request)
        print("The response of CrawlersApi->crawlers_update:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CrawlersApi->crawlers_update: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **crawler** | **str**| The UUID of the crawler | 
 **v2_crawler_request** | [**V2CrawlerRequest**](V2CrawlerRequest.md)|  | 

### Return type

[**V2Crawler**](V2Crawler.md)

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

