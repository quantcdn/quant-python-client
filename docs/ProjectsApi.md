# quantcdn.ProjectsApi

All URIs are relative to *https://dashboard.quantcdn.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_project_logs**](ProjectsApi.md#get_project_logs) | **GET** /api/v2/organizations/{organization}/projects/{project}/logs | Get CDN access logs for a project
[**projects_create**](ProjectsApi.md#projects_create) | **POST** /api/v2/organizations/{organization}/projects | Create a new project
[**projects_delete**](ProjectsApi.md#projects_delete) | **DELETE** /api/v2/organizations/{organization}/projects/{project} | Delete a project
[**projects_list**](ProjectsApi.md#projects_list) | **GET** /api/v2/organizations/{organization}/projects | Retrieve all projects for an organization
[**projects_read**](ProjectsApi.md#projects_read) | **GET** /api/v2/organizations/{organization}/projects/{project} | Get details of a single project
[**projects_update**](ProjectsApi.md#projects_update) | **PATCH** /api/v2/organizations/{organization}/projects/{project} | Update a project


# **get_project_logs**
> GetProjectLogs200Response get_project_logs(organization, project, limit=limit, start_time=start_time, end_time=end_time, filter=filter, domain=domain, next_token=next_token)

Get CDN access logs for a project

Retrieves CloudFront access log entries for an AWS-platform project. Results are always scoped to the project; the optional filter can only narrow them. Entries are returned oldest first; pass nextToken from the previous response to fetch the next page. Logs are retained for 30 days.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.get_project_logs200_response import GetProjectLogs200Response
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
    api_instance = quantcdn.ProjectsApi(api_client)
    organization = 'test-org' # str | The organization machine name
    project = 'test-project' # str | The project machine name
    limit = 100 # int | Maximum number of log entries to return per page (default 100) (optional) (default to 100)
    start_time = '2024-11-16T00:00:00Z' # str | Start of the time range. ISO 8601 or Unix epoch milliseconds. (optional)
    end_time = '2024-11-16T23:59:59Z' # str | End of the time range. ISO 8601 or Unix epoch milliseconds. (optional)
    filter = '$.status_code = 404' # str | CloudWatch JSON filter expression AND-ed with the project constraint, e.g. $.status_code = 404. Outer braces are optional; nested braces are rejected. (optional)
    domain = 'www.example.com' # str | Only return entries for this domain (optional)
    next_token = 'next_token_example' # str | Opaque pagination token from the previous response. Pass back unchanged to fetch the next page. (optional)

    try:
        # Get CDN access logs for a project
        api_response = api_instance.get_project_logs(organization, project, limit=limit, start_time=start_time, end_time=end_time, filter=filter, domain=domain, next_token=next_token)
        print("The response of ProjectsApi->get_project_logs:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ProjectsApi->get_project_logs: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| The organization machine name | 
 **project** | **str**| The project machine name | 
 **limit** | **int**| Maximum number of log entries to return per page (default 100) | [optional] [default to 100]
 **start_time** | **str**| Start of the time range. ISO 8601 or Unix epoch milliseconds. | [optional] 
 **end_time** | **str**| End of the time range. ISO 8601 or Unix epoch milliseconds. | [optional] 
 **filter** | **str**| CloudWatch JSON filter expression AND-ed with the project constraint, e.g. $.status_code &#x3D; 404. Outer braces are optional; nested braces are rejected. | [optional] 
 **domain** | **str**| Only return entries for this domain | [optional] 
 **next_token** | **str**| Opaque pagination token from the previous response. Pass back unchanged to fetch the next page. | [optional] 

### Return type

[**GetProjectLogs200Response**](GetProjectLogs200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Access log entries |  -  |
**400** | Invalid filter or time range |  -  |
**401** | Unauthenticated |  -  |
**403** | Token lacks the projects:read scope or the user lacks browse_projects |  -  |
**404** | The project is not on the AWS platform, or its access logs are not enabled yet |  -  |
**422** | Validation error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **projects_create**
> V2Project projects_create(organization, v2_project_request)

Create a new project

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_project import V2Project
from quantcdn.models.v2_project_request import V2ProjectRequest
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
    api_instance = quantcdn.ProjectsApi(api_client)
    organization = 'test-org' # str | Organization identifier
    v2_project_request = quantcdn.V2ProjectRequest() # V2ProjectRequest | 

    try:
        # Create a new project
        api_response = api_instance.projects_create(organization, v2_project_request)
        print("The response of ProjectsApi->projects_create:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ProjectsApi->projects_create: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **v2_project_request** | [**V2ProjectRequest**](V2ProjectRequest.md)|  | 

### Return type

[**V2Project**](V2Project.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | The request has succeeded and a new resource has been created as a result. |  -  |
**400** | The server could not understand the request due to invalid syntax. |  -  |
**403** | Access is forbidden. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **projects_delete**
> projects_delete(organization, project)

Delete a project

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
    api_instance = quantcdn.ProjectsApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier

    try:
        # Delete a project
        api_instance.projects_delete(organization, project)
    except Exception as e:
        print("Exception when calling ProjectsApi->projects_delete: %s\n" % e)
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
**204** | The request has succeeded. |  -  |
**400** | The server could not understand the request due to invalid syntax. |  -  |
**403** | Access is forbidden. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **projects_list**
> List[V2Project] projects_list(organization)

Retrieve all projects for an organization

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_project import V2Project
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
    api_instance = quantcdn.ProjectsApi(api_client)
    organization = 'test-org' # str | Organization identifier

    try:
        # Retrieve all projects for an organization
        api_response = api_instance.projects_list(organization)
        print("The response of ProjectsApi->projects_list:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ProjectsApi->projects_list: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 

### Return type

[**List[V2Project]**](V2Project.md)

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

# **projects_read**
> V2Project projects_read(organization, project, with_token)

Get details of a single project

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_project import V2Project
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
    api_instance = quantcdn.ProjectsApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    with_token = False # bool |  (default to False)

    try:
        # Get details of a single project
        api_response = api_instance.projects_read(organization, project, with_token)
        print("The response of ProjectsApi->projects_read:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ProjectsApi->projects_read: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **with_token** | **bool**|  | [default to False]

### Return type

[**V2Project**](V2Project.md)

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

# **projects_update**
> V2Project projects_update(organization, project, v2_project_request)

Update a project

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_project import V2Project
from quantcdn.models.v2_project_request import V2ProjectRequest
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
    api_instance = quantcdn.ProjectsApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    v2_project_request = quantcdn.V2ProjectRequest() # V2ProjectRequest | 

    try:
        # Update a project
        api_response = api_instance.projects_update(organization, project, v2_project_request)
        print("The response of ProjectsApi->projects_update:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ProjectsApi->projects_update: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **v2_project_request** | [**V2ProjectRequest**](V2ProjectRequest.md)|  | 

### Return type

[**V2Project**](V2Project.md)

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

