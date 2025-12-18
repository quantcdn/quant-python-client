# quantcdn.CronApi

All URIs are relative to *https://dashboard.quantcdn.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_cron_job**](CronApi.md#create_cron_job) | **POST** /api/v3/organizations/{organisation}/applications/{application}/environments/{environment}/cron | Create a new cron job
[**delete_cron_job**](CronApi.md#delete_cron_job) | **DELETE** /api/v3/organizations/{organisation}/applications/{application}/environments/{environment}/cron/{cron} | Delete a cron job
[**get_cron_job**](CronApi.md#get_cron_job) | **GET** /api/v3/organizations/{organisation}/applications/{application}/environments/{environment}/cron/{cron} | Get a cron job
[**get_cron_run**](CronApi.md#get_cron_run) | **GET** /api/v3/organizations/{organisation}/applications/{application}/environments/{environment}/cron/{cron}/runs/{run} | Get a cron run
[**list_cron_job_runs**](CronApi.md#list_cron_job_runs) | **GET** /api/v3/organizations/{organisation}/applications/{application}/environments/{environment}/cron/{cron}/runs | Get all runs for a cron job
[**list_cron_jobs**](CronApi.md#list_cron_jobs) | **GET** /api/v3/organizations/{organisation}/applications/{application}/environments/{environment}/cron | Get all cron jobs for an environment
[**update_cron_job**](CronApi.md#update_cron_job) | **PATCH** /api/v3/organizations/{organisation}/applications/{application}/environments/{environment}/cron/{cron} | Update a cron job


# **create_cron_job**
> Cron create_cron_job(organisation, application, environment, create_cron_job_request)

Create a new cron job

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.create_cron_job_request import CreateCronJobRequest
from quantcdn.models.cron import Cron
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
    api_instance = quantcdn.CronApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    application = 'application_example' # str | The application ID
    environment = 'environment_example' # str | The environment ID
    create_cron_job_request = quantcdn.CreateCronJobRequest() # CreateCronJobRequest | 

    try:
        # Create a new cron job
        api_response = api_instance.create_cron_job(organisation, application, environment, create_cron_job_request)
        print("The response of CronApi->create_cron_job:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CronApi->create_cron_job: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **application** | **str**| The application ID | 
 **environment** | **str**| The environment ID | 
 **create_cron_job_request** | [**CreateCronJobRequest**](CreateCronJobRequest.md)|  | 

### Return type

[**Cron**](Cron.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | The created cron job |  -  |
**400** | The request is invalid |  -  |
**422** | The request is invalid |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_cron_job**
> delete_cron_job(organisation, application, environment, cron)

Delete a cron job

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
    api_instance = quantcdn.CronApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    application = 'application_example' # str | The application ID
    environment = 'environment_example' # str | The environment ID
    cron = 'cron_example' # str | The cron job ID

    try:
        # Delete a cron job
        api_instance.delete_cron_job(organisation, application, environment, cron)
    except Exception as e:
        print("Exception when calling CronApi->delete_cron_job: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **application** | **str**| The application ID | 
 **environment** | **str**| The environment ID | 
 **cron** | **str**| The cron job ID | 

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
**204** | The cron job deleted |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_cron_job**
> Cron get_cron_job(organisation, application, environment, cron)

Get a cron job

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.cron import Cron
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
    api_instance = quantcdn.CronApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    application = 'application_example' # str | The application ID
    environment = 'environment_example' # str | The environment ID
    cron = 'cron_example' # str | The cron job ID

    try:
        # Get a cron job
        api_response = api_instance.get_cron_job(organisation, application, environment, cron)
        print("The response of CronApi->get_cron_job:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CronApi->get_cron_job: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **application** | **str**| The application ID | 
 **environment** | **str**| The environment ID | 
 **cron** | **str**| The cron job ID | 

### Return type

[**Cron**](Cron.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The cron job |  -  |
**404** | The cron job not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_cron_run**
> CronRun get_cron_run(organisation, application, environment, cron, run)

Get a cron run

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.cron_run import CronRun
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
    api_instance = quantcdn.CronApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    application = 'application_example' # str | The application ID
    environment = 'environment_example' # str | The environment ID
    cron = 'cron_example' # str | The cron job ID
    run = 'run_example' # str | The cron run ID

    try:
        # Get a cron run
        api_response = api_instance.get_cron_run(organisation, application, environment, cron, run)
        print("The response of CronApi->get_cron_run:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CronApi->get_cron_run: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **application** | **str**| The application ID | 
 **environment** | **str**| The environment ID | 
 **cron** | **str**| The cron job ID | 
 **run** | **str**| The cron run ID | 

### Return type

[**CronRun**](CronRun.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The cron run |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_cron_job_runs**
> List[CronRun] list_cron_job_runs(organisation, application, environment, cron)

Get all runs for a cron job

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.cron_run import CronRun
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
    api_instance = quantcdn.CronApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    application = 'application_example' # str | The application ID
    environment = 'environment_example' # str | The environment ID
    cron = 'cron_example' # str | The cron job ID

    try:
        # Get all runs for a cron job
        api_response = api_instance.list_cron_job_runs(organisation, application, environment, cron)
        print("The response of CronApi->list_cron_job_runs:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CronApi->list_cron_job_runs: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **application** | **str**| The application ID | 
 **environment** | **str**| The environment ID | 
 **cron** | **str**| The cron job ID | 

### Return type

[**List[CronRun]**](CronRun.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The runs |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_cron_jobs**
> Cron list_cron_jobs(organisation, application, environment)

Get all cron jobs for an environment

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.cron import Cron
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
    api_instance = quantcdn.CronApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    application = 'application_example' # str | The application ID
    environment = 'environment_example' # str | The environment ID

    try:
        # Get all cron jobs for an environment
        api_response = api_instance.list_cron_jobs(organisation, application, environment)
        print("The response of CronApi->list_cron_jobs:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CronApi->list_cron_jobs: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **application** | **str**| The application ID | 
 **environment** | **str**| The environment ID | 

### Return type

[**Cron**](Cron.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The cron jobs |  -  |
**404** | The environment not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_cron_job**
> Cron update_cron_job(organisation, application, environment, cron, update_cron_job_request)

Update a cron job

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.cron import Cron
from quantcdn.models.update_cron_job_request import UpdateCronJobRequest
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
    api_instance = quantcdn.CronApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    application = 'application_example' # str | The application ID
    environment = 'environment_example' # str | The environment ID
    cron = 'cron_example' # str | The cron job ID
    update_cron_job_request = quantcdn.UpdateCronJobRequest() # UpdateCronJobRequest | 

    try:
        # Update a cron job
        api_response = api_instance.update_cron_job(organisation, application, environment, cron, update_cron_job_request)
        print("The response of CronApi->update_cron_job:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CronApi->update_cron_job: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **application** | **str**| The application ID | 
 **environment** | **str**| The environment ID | 
 **cron** | **str**| The cron job ID | 
 **update_cron_job_request** | [**UpdateCronJobRequest**](UpdateCronJobRequest.md)|  | 

### Return type

[**Cron**](Cron.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The updated cron job |  -  |
**404** | The cron job not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

