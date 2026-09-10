# quantcdn.ResourcesApi

All URIs are relative to *https://dashboard.quantcdn.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**attach_org_resource**](ResourcesApi.md#attach_org_resource) | **POST** /api/v3/organizations/{organisation}/resources/{resource}/attachments | Attach a resource to an application environment
[**create_org_resource**](ResourcesApi.md#create_org_resource) | **POST** /api/v3/organizations/{organisation}/resources | Create a shared resource
[**delete_org_resource**](ResourcesApi.md#delete_org_resource) | **DELETE** /api/v3/organizations/{organisation}/resources/{resource} | Delete a shared resource
[**detach_org_resource**](ResourcesApi.md#detach_org_resource) | **DELETE** /api/v3/organizations/{organisation}/resources/{resource}/attachments/{application}/{environment} | Detach a resource from an application environment
[**get_org_resource**](ResourcesApi.md#get_org_resource) | **GET** /api/v3/organizations/{organisation}/resources/{resource} | Get a shared resource and its attachments
[**get_org_resource_credentials**](ResourcesApi.md#get_org_resource_credentials) | **GET** /api/v3/organizations/{organisation}/resources/{resource}/credentials | Get a cache&#39;s administrative credential
[**list_org_resources**](ResourcesApi.md#list_org_resources) | **GET** /api/v3/organizations/{organisation}/resources | List an organisation&#39;s shared resources
[**purge_org_resource**](ResourcesApi.md#purge_org_resource) | **POST** /api/v3/organizations/{organisation}/resources/{resource}/purge | Purge keys from a cache


# **attach_org_resource**
> ResourceAttachment attach_org_resource(organisation, resource, attach_org_resource_request)

Attach a resource to an application environment

Object storage credentials are written immediately and take effect on the environment's next deploy. Cache variables are rendered at the next deploy, so a cache may be attached while it is still provisioning. An environment accepts one attachment per resource type.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.attach_org_resource_request import AttachOrgResourceRequest
from quantcdn.models.resource_attachment import ResourceAttachment
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
    api_instance = quantcdn.ResourcesApi(api_client)
    organisation = 'test-org' # str | The organisation ID
    resource = 'res-abc123' # str | The resource ID
    attach_org_resource_request = quantcdn.AttachOrgResourceRequest() # AttachOrgResourceRequest | 

    try:
        # Attach a resource to an application environment
        api_response = api_instance.attach_org_resource(organisation, resource, attach_org_resource_request)
        print("The response of ResourcesApi->attach_org_resource:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ResourcesApi->attach_org_resource: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **resource** | **str**| The resource ID | 
 **attach_org_resource_request** | [**AttachOrgResourceRequest**](AttachOrgResourceRequest.md)|  | 

### Return type

[**ResourceAttachment**](ResourceAttachment.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The attachment |  -  |
**409** | An attachment of this type already exists for the environment |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_org_resource**
> OrgResource create_org_resource(organisation, create_org_resource_request)

Create a shared resource

Object storage is provisioned synchronously and returns status available. A Valkey cache is asynchronous and returns status provisioning; poll the show endpoint until it reports available.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.create_org_resource_request import CreateOrgResourceRequest
from quantcdn.models.org_resource import OrgResource
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
    api_instance = quantcdn.ResourcesApi(api_client)
    organisation = 'test-org' # str | The organisation ID
    create_org_resource_request = quantcdn.CreateOrgResourceRequest() # CreateOrgResourceRequest | 

    try:
        # Create a shared resource
        api_response = api_instance.create_org_resource(organisation, create_org_resource_request)
        print("The response of ResourcesApi->create_org_resource:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ResourcesApi->create_org_resource: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **create_org_resource_request** | [**CreateOrgResourceRequest**](CreateOrgResourceRequest.md)|  | 

### Return type

[**OrgResource**](OrgResource.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | The created resource |  -  |
**422** | Invalid type, name or cache capacity |  -  |
**409** | A resource with this name already exists |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_org_resource**
> delete_org_resource(organisation, resource, force=force)

Delete a shared resource

Deletes the resource and its contents. This cannot be undone. A resource with live attachments is rejected unless force is set.

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
    api_instance = quantcdn.ResourcesApi(api_client)
    organisation = 'test-org' # str | The organisation ID
    resource = 'res-abc123' # str | The resource ID
    force = True # bool | Delete even if the resource is attached or in an error state (optional)

    try:
        # Delete a shared resource
        api_instance.delete_org_resource(organisation, resource, force=force)
    except Exception as e:
        print("Exception when calling ResourcesApi->delete_org_resource: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **resource** | **str**| The resource ID | 
 **force** | **bool**| Delete even if the resource is attached or in an error state | [optional] 

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
**204** | Deleted |  -  |
**409** | The resource is still attached |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **detach_org_resource**
> detach_org_resource(organisation, resource, application, environment)

Detach a resource from an application environment

Removes the injected credentials and redeploys the environment so that it stops referencing them, which interrupts the environment briefly. The resource and its contents are not deleted.

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
    api_instance = quantcdn.ResourcesApi(api_client)
    organisation = 'test-org' # str | The organisation ID
    resource = 'res-abc123' # str | The resource ID
    application = 'test-app' # str | The application ID
    environment = 'production' # str | The environment ID

    try:
        # Detach a resource from an application environment
        api_instance.detach_org_resource(organisation, resource, application, environment)
    except Exception as e:
        print("Exception when calling ResourcesApi->detach_org_resource: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **resource** | **str**| The resource ID | 
 **application** | **str**| The application ID | 
 **environment** | **str**| The environment ID | 

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
**204** | Detached; the environment is redeploying |  -  |
**404** | No such attachment |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_org_resource**
> OrgResource get_org_resource(organisation, resource)

Get a shared resource and its attachments

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.org_resource import OrgResource
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
    api_instance = quantcdn.ResourcesApi(api_client)
    organisation = 'test-org' # str | The organisation ID
    resource = 'res-abc123' # str | The resource ID

    try:
        # Get a shared resource and its attachments
        api_response = api_instance.get_org_resource(organisation, resource)
        print("The response of ResourcesApi->get_org_resource:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ResourcesApi->get_org_resource: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **resource** | **str**| The resource ID | 

### Return type

[**OrgResource**](OrgResource.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The resource |  -  |
**404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_org_resource_credentials**
> GetOrgResourceCredentials200Response get_org_resource_credentials(organisation, resource)

Get a cache's administrative credential

Cache resources only. Returns the cache-wide user (every key, every command, including FLUSHDB) with host and port. Environments attached to the cache use their own scoped users; this credential is for operators who genuinely need unrestricted access. Every read is audit-logged against the requesting user.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.get_org_resource_credentials200_response import GetOrgResourceCredentials200Response
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
    api_instance = quantcdn.ResourcesApi(api_client)
    organisation = 'test-org' # str | The organisation ID
    resource = 'vk-sessions' # str | The resource ID

    try:
        # Get a cache's administrative credential
        api_response = api_instance.get_org_resource_credentials(organisation, resource)
        print("The response of ResourcesApi->get_org_resource_credentials:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ResourcesApi->get_org_resource_credentials: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **resource** | **str**| The resource ID | 

### Return type

[**GetOrgResourceCredentials200Response**](GetOrgResourceCredentials200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The admin credential |  -  |
**409** | Not a cache resource, or not yet available |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_org_resources**
> List[OrgResource] list_org_resources(organisation)

List an organisation's shared resources

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.org_resource import OrgResource
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
    api_instance = quantcdn.ResourcesApi(api_client)
    organisation = 'test-org' # str | The organisation ID

    try:
        # List an organisation's shared resources
        api_response = api_instance.list_org_resources(organisation)
        print("The response of ResourcesApi->list_org_resources:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ResourcesApi->list_org_resources: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 

### Return type

[**List[OrgResource]**](OrgResource.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The organisation&#39;s resources |  -  |
**403** | Cloud access required |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **purge_org_resource**
> PurgeOrgResource200Response purge_org_resource(organisation, resource, purge_org_resource_request)

Purge keys from a cache

Cache resources only. scope environment deletes that environment's keys, using the CACHE_PREFIX recorded on its attachment rather than anything in the request. scope all flushes every key for every attached environment and requires confirm=true. A large environment purge may return complete=false with a cursor to resume.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.purge_org_resource200_response import PurgeOrgResource200Response
from quantcdn.models.purge_org_resource_request import PurgeOrgResourceRequest
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
    api_instance = quantcdn.ResourcesApi(api_client)
    organisation = 'test-org' # str | The organisation ID
    resource = 'vk-sessions' # str | The resource ID
    purge_org_resource_request = quantcdn.PurgeOrgResourceRequest() # PurgeOrgResourceRequest | 

    try:
        # Purge keys from a cache
        api_response = api_instance.purge_org_resource(organisation, resource, purge_org_resource_request)
        print("The response of ResourcesApi->purge_org_resource:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ResourcesApi->purge_org_resource: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **resource** | **str**| The resource ID | 
 **purge_org_resource_request** | [**PurgeOrgResourceRequest**](PurgeOrgResourceRequest.md)|  | 

### Return type

[**PurgeOrgResource200Response**](PurgeOrgResource200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Purge result |  -  |
**422** | Invalid scope, missing application/environment, or scope all without confirm |  -  |
**404** | No such attachment |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

