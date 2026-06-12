# quantcdn.AISearchApi

All URIs are relative to *https://dashboard.quantcdn.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**ai_search_chat**](AISearchApi.md#ai_search_chat) | **POST** /api/v3/organisations/{organisation}/projects/{project}/ai-search/chat | RAG chat with AI Search content
[**ai_search_delete_pages**](AISearchApi.md#ai_search_delete_pages) | **DELETE** /api/v3/organisations/{organisation}/projects/{project}/ai-search/pages | Delete pages by URLs or patterns
[**ai_search_disable**](AISearchApi.md#ai_search_disable) | **POST** /api/v3/organisations/{organisation}/projects/{project}/ai-search/disable | Disable AI Search for a project
[**ai_search_enable**](AISearchApi.md#ai_search_enable) | **POST** /api/v3/organisations/{organisation}/projects/{project}/ai-search/enable | Enable AI Search for a project
[**ai_search_get_crawl**](AISearchApi.md#ai_search_get_crawl) | **GET** /api/v3/organisations/{organisation}/projects/{project}/ai-search/crawls/{jobId} | Get AI Search ingest job status
[**ai_search_get_crawl_pages**](AISearchApi.md#ai_search_get_crawl_pages) | **GET** /api/v3/organisations/{organisation}/projects/{project}/ai-search/crawls/{jobId}/pages | Get per-page ingest results for a crawl job
[**ai_search_get_settings**](AISearchApi.md#ai_search_get_settings) | **GET** /api/v3/organisations/{organisation}/projects/{project}/ai-search/settings | Get AI Search public access and rate limit settings
[**ai_search_ingest_pages**](AISearchApi.md#ai_search_ingest_pages) | **POST** /api/v3/organisations/{organisation}/projects/{project}/ai-search/pages | Ingest pages into the AI Search index
[**ai_search_list_crawls**](AISearchApi.md#ai_search_list_crawls) | **GET** /api/v3/organisations/{organisation}/projects/{project}/ai-search/crawls | List AI Search ingest jobs
[**ai_search_list_pages**](AISearchApi.md#ai_search_list_pages) | **GET** /api/v3/organisations/{organisation}/projects/{project}/ai-search/pages | List indexed pages with cursor pagination
[**ai_search_purge_index**](AISearchApi.md#ai_search_purge_index) | **DELETE** /api/v3/organisations/{organisation}/projects/{project}/ai-search/index | Purge the entire AI Search index
[**ai_search_search**](AISearchApi.md#ai_search_search) | **POST** /api/v3/organisations/{organisation}/projects/{project}/ai-search/search | Semantic search across the AI Search index
[**ai_search_status**](AISearchApi.md#ai_search_status) | **GET** /api/v3/organisations/{organisation}/projects/{project}/ai-search | Get AI Search status for a project
[**ai_search_top_queries**](AISearchApi.md#ai_search_top_queries) | **GET** /api/v3/organisations/{organisation}/projects/{project}/ai-search/top-queries | Get the most popular AI Search queries
[**ai_search_trigger_crawl**](AISearchApi.md#ai_search_trigger_crawl) | **POST** /api/v3/organisations/{organisation}/projects/{project}/ai-search/crawls | Trigger a crawler run that ingests into AI Search
[**ai_search_update_settings**](AISearchApi.md#ai_search_update_settings) | **PUT** /api/v3/organisations/{organisation}/projects/{project}/ai-search/settings | Update AI Search public access and rate limit settings
[**ai_search_usage**](AISearchApi.md#ai_search_usage) | **GET** /api/v3/organisations/{organisation}/projects/{project}/ai-search/usage | Get usage statistics for the AI Search site


# **ai_search_chat**
> ai_search_chat(organisation, project, ai_search_chat_request)

RAG chat with AI Search content

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.ai_search_chat_request import AiSearchChatRequest
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
    api_instance = quantcdn.AISearchApi(api_client)
    organisation = 'organisation_example' # str | 
    project = 'project_example' # str | 
    ai_search_chat_request = quantcdn.AiSearchChatRequest() # AiSearchChatRequest | 

    try:
        # RAG chat with AI Search content
        api_instance.ai_search_chat(organisation, project, ai_search_chat_request)
    except Exception as e:
        print("Exception when calling AISearchApi->ai_search_chat: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**|  | 
 **project** | **str**|  | 
 **ai_search_chat_request** | [**AiSearchChatRequest**](AiSearchChatRequest.md)|  | 

### Return type

void (empty response body)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Chat reply |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ai_search_delete_pages**
> ai_search_delete_pages(organisation, project, ai_search_delete_pages_request)

Delete pages by URLs or patterns

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.ai_search_delete_pages_request import AiSearchDeletePagesRequest
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
    api_instance = quantcdn.AISearchApi(api_client)
    organisation = 'organisation_example' # str | 
    project = 'project_example' # str | 
    ai_search_delete_pages_request = quantcdn.AiSearchDeletePagesRequest() # AiSearchDeletePagesRequest | 

    try:
        # Delete pages by URLs or patterns
        api_instance.ai_search_delete_pages(organisation, project, ai_search_delete_pages_request)
    except Exception as e:
        print("Exception when calling AISearchApi->ai_search_delete_pages: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**|  | 
 **project** | **str**|  | 
 **ai_search_delete_pages_request** | [**AiSearchDeletePagesRequest**](AiSearchDeletePagesRequest.md)|  | 

### Return type

void (empty response body)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Deleted |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ai_search_disable**
> ai_search_disable(organisation, project)

Disable AI Search for a project

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
    api_instance = quantcdn.AISearchApi(api_client)
    organisation = 'organisation_example' # str | 
    project = 'project_example' # str | 

    try:
        # Disable AI Search for a project
        api_instance.ai_search_disable(organisation, project)
    except Exception as e:
        print("Exception when calling AISearchApi->ai_search_disable: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**|  | 
 **project** | **str**|  | 

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
**200** | Disabled |  -  |
**404** | Not enabled |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ai_search_enable**
> ai_search_enable(organisation, project, ai_search_enable_request=ai_search_enable_request)

Enable AI Search for a project

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.ai_search_enable_request import AiSearchEnableRequest
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
    api_instance = quantcdn.AISearchApi(api_client)
    organisation = 'organisation_example' # str | 
    project = 'project_example' # str | 
    ai_search_enable_request = quantcdn.AiSearchEnableRequest() # AiSearchEnableRequest |  (optional)

    try:
        # Enable AI Search for a project
        api_instance.ai_search_enable(organisation, project, ai_search_enable_request=ai_search_enable_request)
    except Exception as e:
        print("Exception when calling AISearchApi->ai_search_enable: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**|  | 
 **project** | **str**|  | 
 **ai_search_enable_request** | [**AiSearchEnableRequest**](AiSearchEnableRequest.md)|  | [optional] 

### Return type

void (empty response body)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Enabled |  -  |
**400** | Missing base URL |  -  |
**409** | Already enabled |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ai_search_get_crawl**
> ai_search_get_crawl(organisation, project, job_id)

Get AI Search ingest job status

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
    api_instance = quantcdn.AISearchApi(api_client)
    organisation = 'organisation_example' # str | 
    project = 'project_example' # str | 
    job_id = 'job_id_example' # str | 

    try:
        # Get AI Search ingest job status
        api_instance.ai_search_get_crawl(organisation, project, job_id)
    except Exception as e:
        print("Exception when calling AISearchApi->ai_search_get_crawl: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**|  | 
 **project** | **str**|  | 
 **job_id** | **str**|  | 

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
**200** | Job status |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ai_search_get_crawl_pages**
> ai_search_get_crawl_pages(organisation, project, job_id, limit=limit, status_code=status_code, processing_status=processing_status)

Get per-page ingest results for a crawl job

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
    api_instance = quantcdn.AISearchApi(api_client)
    organisation = 'organisation_example' # str | 
    project = 'project_example' # str | 
    job_id = 'job_id_example' # str | 
    limit = 56 # int |  (optional)
    status_code = 56 # int |  (optional)
    processing_status = 'processing_status_example' # str |  (optional)

    try:
        # Get per-page ingest results for a crawl job
        api_instance.ai_search_get_crawl_pages(organisation, project, job_id, limit=limit, status_code=status_code, processing_status=processing_status)
    except Exception as e:
        print("Exception when calling AISearchApi->ai_search_get_crawl_pages: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**|  | 
 **project** | **str**|  | 
 **job_id** | **str**|  | 
 **limit** | **int**|  | [optional] 
 **status_code** | **int**|  | [optional] 
 **processing_status** | **str**|  | [optional] 

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
**200** | Pages |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ai_search_get_settings**
> ai_search_get_settings(organisation, project)

Get AI Search public access and rate limit settings

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
    api_instance = quantcdn.AISearchApi(api_client)
    organisation = 'organisation_example' # str | 
    project = 'project_example' # str | 

    try:
        # Get AI Search public access and rate limit settings
        api_instance.ai_search_get_settings(organisation, project)
    except Exception as e:
        print("Exception when calling AISearchApi->ai_search_get_settings: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**|  | 
 **project** | **str**|  | 

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
**200** | Settings |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ai_search_ingest_pages**
> ai_search_ingest_pages(organisation, project, ai_search_ingest_pages_request)

Ingest pages into the AI Search index

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.ai_search_ingest_pages_request import AiSearchIngestPagesRequest
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
    api_instance = quantcdn.AISearchApi(api_client)
    organisation = 'organisation_example' # str | 
    project = 'project_example' # str | 
    ai_search_ingest_pages_request = quantcdn.AiSearchIngestPagesRequest() # AiSearchIngestPagesRequest | 

    try:
        # Ingest pages into the AI Search index
        api_instance.ai_search_ingest_pages(organisation, project, ai_search_ingest_pages_request)
    except Exception as e:
        print("Exception when calling AISearchApi->ai_search_ingest_pages: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**|  | 
 **project** | **str**|  | 
 **ai_search_ingest_pages_request** | [**AiSearchIngestPagesRequest**](AiSearchIngestPagesRequest.md)|  | 

### Return type

void (empty response body)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Pages processed |  -  |
**422** | Validation failed |  -  |
**502** | Upstream failure |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ai_search_list_crawls**
> ai_search_list_crawls(organisation, project, limit=limit)

List AI Search ingest jobs

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
    api_instance = quantcdn.AISearchApi(api_client)
    organisation = 'organisation_example' # str | 
    project = 'project_example' # str | 
    limit = 56 # int |  (optional)

    try:
        # List AI Search ingest jobs
        api_instance.ai_search_list_crawls(organisation, project, limit=limit)
    except Exception as e:
        print("Exception when calling AISearchApi->ai_search_list_crawls: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**|  | 
 **project** | **str**|  | 
 **limit** | **int**|  | [optional] 

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
**200** | Jobs |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ai_search_list_pages**
> ai_search_list_pages(organisation, project, limit=limit, cursor=cursor, search=search)

List indexed pages with cursor pagination

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
    api_instance = quantcdn.AISearchApi(api_client)
    organisation = 'organisation_example' # str | 
    project = 'project_example' # str | 
    limit = 56 # int |  (optional)
    cursor = 'cursor_example' # str |  (optional)
    search = 'search_example' # str |  (optional)

    try:
        # List indexed pages with cursor pagination
        api_instance.ai_search_list_pages(organisation, project, limit=limit, cursor=cursor, search=search)
    except Exception as e:
        print("Exception when calling AISearchApi->ai_search_list_pages: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**|  | 
 **project** | **str**|  | 
 **limit** | **int**|  | [optional] 
 **cursor** | **str**|  | [optional] 
 **search** | **str**|  | [optional] 

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
**200** | Pages |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ai_search_purge_index**
> ai_search_purge_index(organisation, project)

Purge the entire AI Search index

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
    api_instance = quantcdn.AISearchApi(api_client)
    organisation = 'organisation_example' # str | 
    project = 'project_example' # str | 

    try:
        # Purge the entire AI Search index
        api_instance.ai_search_purge_index(organisation, project)
    except Exception as e:
        print("Exception when calling AISearchApi->ai_search_purge_index: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**|  | 
 **project** | **str**|  | 

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
**200** | Purged |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ai_search_search**
> ai_search_search(organisation, project, ai_search_search_request)

Semantic search across the AI Search index

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.ai_search_search_request import AiSearchSearchRequest
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
    api_instance = quantcdn.AISearchApi(api_client)
    organisation = 'organisation_example' # str | 
    project = 'project_example' # str | 
    ai_search_search_request = quantcdn.AiSearchSearchRequest() # AiSearchSearchRequest | 

    try:
        # Semantic search across the AI Search index
        api_instance.ai_search_search(organisation, project, ai_search_search_request)
    except Exception as e:
        print("Exception when calling AISearchApi->ai_search_search: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**|  | 
 **project** | **str**|  | 
 **ai_search_search_request** | [**AiSearchSearchRequest**](AiSearchSearchRequest.md)|  | 

### Return type

void (empty response body)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Results |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ai_search_status**
> ai_search_status(organisation, project)

Get AI Search status for a project

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
    api_instance = quantcdn.AISearchApi(api_client)
    organisation = 'organisation_example' # str | 
    project = 'project_example' # str | 

    try:
        # Get AI Search status for a project
        api_instance.ai_search_status(organisation, project)
    except Exception as e:
        print("Exception when calling AISearchApi->ai_search_status: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**|  | 
 **project** | **str**|  | 

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
**200** | Status |  -  |
**401** | Unauthorized |  -  |
**403** | Forbidden |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ai_search_top_queries**
> ai_search_top_queries(organisation, project, range=range, limit=limit)

Get the most popular AI Search queries

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
    api_instance = quantcdn.AISearchApi(api_client)
    organisation = 'organisation_example' # str | 
    project = 'project_example' # str | 
    range = '30d' # str |  (optional) (default to '30d')
    limit = 56 # int |  (optional)

    try:
        # Get the most popular AI Search queries
        api_instance.ai_search_top_queries(organisation, project, range=range, limit=limit)
    except Exception as e:
        print("Exception when calling AISearchApi->ai_search_top_queries: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**|  | 
 **project** | **str**|  | 
 **range** | **str**|  | [optional] [default to &#39;30d&#39;]
 **limit** | **int**|  | [optional] 

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
**200** | Top queries |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ai_search_trigger_crawl**
> ai_search_trigger_crawl(organisation, project, ai_search_trigger_crawl_request)

Trigger a crawler run that ingests into AI Search

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.ai_search_trigger_crawl_request import AiSearchTriggerCrawlRequest
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
    api_instance = quantcdn.AISearchApi(api_client)
    organisation = 'organisation_example' # str | 
    project = 'project_example' # str | 
    ai_search_trigger_crawl_request = quantcdn.AiSearchTriggerCrawlRequest() # AiSearchTriggerCrawlRequest | 

    try:
        # Trigger a crawler run that ingests into AI Search
        api_instance.ai_search_trigger_crawl(organisation, project, ai_search_trigger_crawl_request)
    except Exception as e:
        print("Exception when calling AISearchApi->ai_search_trigger_crawl: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**|  | 
 **project** | **str**|  | 
 **ai_search_trigger_crawl_request** | [**AiSearchTriggerCrawlRequest**](AiSearchTriggerCrawlRequest.md)|  | 

### Return type

void (empty response body)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Crawl started |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ai_search_update_settings**
> ai_search_update_settings(organisation, project, ai_search_update_settings_request)

Update AI Search public access and rate limit settings

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.ai_search_update_settings_request import AiSearchUpdateSettingsRequest
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
    api_instance = quantcdn.AISearchApi(api_client)
    organisation = 'organisation_example' # str | 
    project = 'project_example' # str | 
    ai_search_update_settings_request = quantcdn.AiSearchUpdateSettingsRequest() # AiSearchUpdateSettingsRequest | 

    try:
        # Update AI Search public access and rate limit settings
        api_instance.ai_search_update_settings(organisation, project, ai_search_update_settings_request)
    except Exception as e:
        print("Exception when calling AISearchApi->ai_search_update_settings: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**|  | 
 **project** | **str**|  | 
 **ai_search_update_settings_request** | [**AiSearchUpdateSettingsRequest**](AiSearchUpdateSettingsRequest.md)|  | 

### Return type

void (empty response body)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Updated |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ai_search_usage**
> ai_search_usage(organisation, project, range=range)

Get usage statistics for the AI Search site

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
    api_instance = quantcdn.AISearchApi(api_client)
    organisation = 'organisation_example' # str | 
    project = 'project_example' # str | 
    range = '30d' # str |  (optional) (default to '30d')

    try:
        # Get usage statistics for the AI Search site
        api_instance.ai_search_usage(organisation, project, range=range)
    except Exception as e:
        print("Exception when calling AISearchApi->ai_search_usage: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**|  | 
 **project** | **str**|  | 
 **range** | **str**|  | [optional] [default to &#39;30d&#39;]

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
**200** | Usage |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

