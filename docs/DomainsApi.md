# quantcdn.DomainsApi

All URIs are relative to *https://dashboard.quantcdn.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**d_ns_create_record**](DomainsApi.md#d_ns_create_record) | **POST** /api/v2/organizations/{organization}/dns/zones/{zoneId}/records | Create an A record
[**d_ns_list_records**](DomainsApi.md#d_ns_list_records) | **GET** /api/v2/organizations/{organization}/dns/zones/{zoneId}/records | List DNS records
[**d_ns_list_zones**](DomainsApi.md#d_ns_list_zones) | **GET** /api/v2/organizations/{organization}/dns/zones | List organization DNS zones
[**d_ns_show_zone**](DomainsApi.md#d_ns_show_zone) | **GET** /api/v2/organizations/{organization}/dns/zones/{zoneId} | Get a DNS zone
[**domains_create**](DomainsApi.md#domains_create) | **POST** /api/v2/organizations/{organization}/projects/{project}/domains | Add a new domain
[**domains_delete**](DomainsApi.md#domains_delete) | **DELETE** /api/v2/organizations/{organization}/projects/{project}/domains/{domain} | Delete a domain
[**domains_list**](DomainsApi.md#domains_list) | **GET** /api/v2/organizations/{organization}/projects/{project}/domains | List all domains for a project
[**domains_read**](DomainsApi.md#domains_read) | **GET** /api/v2/organizations/{organization}/projects/{project}/domains/{domain} | Get details of a single domain
[**domains_renew**](DomainsApi.md#domains_renew) | **POST** /api/v2/organizations/{organization}/projects/{project}/domains/{domain}/renew | Renew the SSL certificate for a domain


# **d_ns_create_record**
> d_ns_create_record(organization, zone_id, dns_create_record_request)

Create an A record

dns:write and add_domains are required. Existing names are rejected; this endpoint does not update records. Only organization-wide tokens are accepted.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.dns_create_record_request import DNSCreateRecordRequest
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
    api_instance = quantcdn.DomainsApi(api_client)
    organization = 'organization_example' # str | 
    zone_id = 'zone_id_example' # str | 
    dns_create_record_request = quantcdn.DNSCreateRecordRequest() # DNSCreateRecordRequest | 

    try:
        # Create an A record
        api_instance.d_ns_create_record(organization, zone_id, dns_create_record_request)
    except Exception as e:
        print("Exception when calling DomainsApi->d_ns_create_record: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**|  | 
 **zone_id** | **str**|  | 
 **dns_create_record_request** | [**DNSCreateRecordRequest**](DNSCreateRecordRequest.md)|  | 

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
**201** | Success |  -  |
**401** | Missing or invalid API token |  -  |
**403** | Token scope, organization or role permission denied |  -  |
**404** | Zone not found in this organization |  -  |
**409** | A record already exists for this name |  -  |
**422** | Invalid request |  -  |
**503** | DNS service unavailable |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **d_ns_list_records**
> d_ns_list_records(organization, zone_id, type=type, name=name, limit=limit, offset=offset, sync=sync)

List DNS records

dns:read and browse_domains are required. Filters: type, name, limit (1–1000), offset, sync (true/false).

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
    api_instance = quantcdn.DomainsApi(api_client)
    organization = 'organization_example' # str | 
    zone_id = 'zone_id_example' # str | 
    type = 'type_example' # str |  (optional)
    name = 'name_example' # str |  (optional)
    limit = 100 # int |  (optional) (default to 100)
    offset = 0 # int |  (optional) (default to 0)
    sync = False # bool |  (optional) (default to False)

    try:
        # List DNS records
        api_instance.d_ns_list_records(organization, zone_id, type=type, name=name, limit=limit, offset=offset, sync=sync)
    except Exception as e:
        print("Exception when calling DomainsApi->d_ns_list_records: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**|  | 
 **zone_id** | **str**|  | 
 **type** | **str**|  | [optional] 
 **name** | **str**|  | [optional] 
 **limit** | **int**|  | [optional] [default to 100]
 **offset** | **int**|  | [optional] [default to 0]
 **sync** | **bool**|  | [optional] [default to False]

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
**200** | Success |  -  |
**401** | Missing or invalid API token |  -  |
**403** | Token scope, organization or role permission denied |  -  |
**404** | Zone not found in this organization |  -  |
**409** | A record already exists for this name |  -  |
**422** | Invalid request |  -  |
**503** | DNS service unavailable |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **d_ns_list_zones**
> d_ns_list_zones(organization)

List organization DNS zones

dns:read and browse_domains are required.

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
    api_instance = quantcdn.DomainsApi(api_client)
    organization = 'organization_example' # str | 

    try:
        # List organization DNS zones
        api_instance.d_ns_list_zones(organization)
    except Exception as e:
        print("Exception when calling DomainsApi->d_ns_list_zones: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**|  | 

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
**200** | Success |  -  |
**401** | Missing or invalid API token |  -  |
**403** | Token scope, organization or role permission denied |  -  |
**404** | Zone not found in this organization |  -  |
**409** | A record already exists for this name |  -  |
**422** | Invalid request |  -  |
**503** | DNS service unavailable |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **d_ns_show_zone**
> d_ns_show_zone(organization, zone_id)

Get a DNS zone

dns:read and browse_domains are required. The zone must belong to the organization.

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
    api_instance = quantcdn.DomainsApi(api_client)
    organization = 'organization_example' # str | 
    zone_id = 'zone_id_example' # str | 

    try:
        # Get a DNS zone
        api_instance.d_ns_show_zone(organization, zone_id)
    except Exception as e:
        print("Exception when calling DomainsApi->d_ns_show_zone: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**|  | 
 **zone_id** | **str**|  | 

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
**200** | Success |  -  |
**401** | Missing or invalid API token |  -  |
**403** | Token scope, organization or role permission denied |  -  |
**404** | Zone not found in this organization |  -  |
**409** | A record already exists for this name |  -  |
**422** | Invalid request |  -  |
**503** | DNS service unavailable |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **domains_create**
> V2Domain domains_create(organization, project, v2_domain_request)

Add a new domain

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_domain import V2Domain
from quantcdn.models.v2_domain_request import V2DomainRequest
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
    api_instance = quantcdn.DomainsApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    v2_domain_request = quantcdn.V2DomainRequest() # V2DomainRequest | 

    try:
        # Add a new domain
        api_response = api_instance.domains_create(organization, project, v2_domain_request)
        print("The response of DomainsApi->domains_create:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DomainsApi->domains_create: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **v2_domain_request** | [**V2DomainRequest**](V2DomainRequest.md)|  | 

### Return type

[**V2Domain**](V2Domain.md)

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

# **domains_delete**
> domains_delete(organization, project, domain)

Delete a domain

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
    api_instance = quantcdn.DomainsApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    domain = '0000' # str | Domain id

    try:
        # Delete a domain
        api_instance.domains_delete(organization, project, domain)
    except Exception as e:
        print("Exception when calling DomainsApi->domains_delete: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **domain** | **str**| Domain id | 

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
**204** | The domain has been deleted. |  -  |
**400** | The server could not understand the request due to invalid syntax. |  -  |
**403** | Access is forbidden. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **domains_list**
> List[V2Domain] domains_list(organization, project)

List all domains for a project

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_domain import V2Domain
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
    api_instance = quantcdn.DomainsApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier

    try:
        # List all domains for a project
        api_response = api_instance.domains_list(organization, project)
        print("The response of DomainsApi->domains_list:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DomainsApi->domains_list: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 

### Return type

[**List[V2Domain]**](V2Domain.md)

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

# **domains_read**
> V2Domain domains_read(organization, project, domain)

Get details of a single domain

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_domain import V2Domain
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
    api_instance = quantcdn.DomainsApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    domain = '0000' # str | Domain id

    try:
        # Get details of a single domain
        api_response = api_instance.domains_read(organization, project, domain)
        print("The response of DomainsApi->domains_read:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DomainsApi->domains_read: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **domain** | **str**| Domain id | 

### Return type

[**V2Domain**](V2Domain.md)

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

# **domains_renew**
> domains_renew(organization, project, domain)

Renew the SSL certificate for a domain

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
    api_instance = quantcdn.DomainsApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    domain = '0000' # str | Domain id

    try:
        # Renew the SSL certificate for a domain
        api_instance.domains_renew(organization, project, domain)
    except Exception as e:
        print("Exception when calling DomainsApi->domains_renew: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **domain** | **str**| Domain id | 

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
**202** | The SSL certificate renewal has been initiated. |  -  |
**400** | The server could not understand the request due to invalid syntax. |  -  |
**403** | Access is forbidden. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

