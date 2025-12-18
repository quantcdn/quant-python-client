# quantcdn.KVApi

All URIs are relative to *https://dashboard.quantcdn.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**k_v_create**](KVApi.md#k_v_create) | **POST** /api/v2/organizations/{organization}/projects/{project}/kv | Add a kv store
[**k_v_delete**](KVApi.md#k_v_delete) | **DELETE** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id} | Delete a kv store
[**k_v_items_create**](KVApi.md#k_v_items_create) | **POST** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id}/items | Add an item to a kv store
[**k_v_items_delete**](KVApi.md#k_v_items_delete) | **DELETE** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id}/items/{key} | Delete an item from a kv store
[**k_v_items_list**](KVApi.md#k_v_items_list) | **GET** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id}/items | List items in a kv store
[**k_v_items_show**](KVApi.md#k_v_items_show) | **GET** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id}/items/{key} | Get an item from a kv store
[**k_v_items_update**](KVApi.md#k_v_items_update) | **PUT** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id}/items/{key} | Update an item in a kv store
[**k_v_list**](KVApi.md#k_v_list) | **GET** /api/v2/organizations/{organization}/projects/{project}/kv | List key-value stores
[**k_v_show**](KVApi.md#k_v_show) | **GET** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id} | Get a kv store


# **k_v_create**
> V2Store k_v_create(organization, project, v2_store_request)

Add a kv store

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_store import V2Store
from quantcdn.models.v2_store_request import V2StoreRequest
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    v2_store_request = quantcdn.V2StoreRequest() # V2StoreRequest | 

    try:
        # Add a kv store
        api_response = api_instance.k_v_create(organization, project, v2_store_request)
        print("The response of KVApi->k_v_create:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_create: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **v2_store_request** | [**V2StoreRequest**](V2StoreRequest.md)|  | 

### Return type

[**V2Store**](V2Store.md)

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

# **k_v_delete**
> k_v_delete(organization, project, store_id)

Delete a kv store

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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = '0000' # str | 

    try:
        # Delete a kv store
        api_instance.k_v_delete(organization, project, store_id)
    except Exception as e:
        print("Exception when calling KVApi->k_v_delete: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**|  | 

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

# **k_v_items_create**
> KVItemsCreate200Response k_v_items_create(organization, project, store_id, v2_store_item_request)

Add an item to a kv store

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.kv_items_create200_response import KVItemsCreate200Response
from quantcdn.models.v2_store_item_request import V2StoreItemRequest
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = '0000' # str | 
    v2_store_item_request = quantcdn.V2StoreItemRequest() # V2StoreItemRequest | 

    try:
        # Add an item to a kv store
        api_response = api_instance.k_v_items_create(organization, project, store_id, v2_store_item_request)
        print("The response of KVApi->k_v_items_create:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_items_create: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**|  | 
 **v2_store_item_request** | [**V2StoreItemRequest**](V2StoreItemRequest.md)|  | 

### Return type

[**KVItemsCreate200Response**](KVItemsCreate200Response.md)

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
**422** | Validation error. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_items_delete**
> KVItemsDelete200Response k_v_items_delete(organization, project, store_id, key)

Delete an item from a kv store

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.kv_items_delete200_response import KVItemsDelete200Response
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = '0000' # str | 
    key = 'key_example' # str | 

    try:
        # Delete an item from a kv store
        api_response = api_instance.k_v_items_delete(organization, project, store_id, key)
        print("The response of KVApi->k_v_items_delete:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_items_delete: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**|  | 
 **key** | **str**|  | 

### Return type

[**KVItemsDelete200Response**](KVItemsDelete200Response.md)

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

# **k_v_items_list**
> V2StoreItemsListResponse k_v_items_list(organization, project, store_id, cursor=cursor, limit=limit, search=search, include_values=include_values)

List items in a kv store

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_store_items_list_response import V2StoreItemsListResponse
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = '0000' # str | 
    cursor = 'cursor_example' # str | Cursor for pagination (optional)
    limit = 10 # int | Number of items to return (optional) (default to 10)
    search = 'search_example' # str | Search filter for keys (optional)
    include_values = False # bool | Include values in the response. Secret values will be redacted as '[ENCRYPTED]' for security. (optional) (default to False)

    try:
        # List items in a kv store
        api_response = api_instance.k_v_items_list(organization, project, store_id, cursor=cursor, limit=limit, search=search, include_values=include_values)
        print("The response of KVApi->k_v_items_list:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_items_list: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**|  | 
 **cursor** | **str**| Cursor for pagination | [optional] 
 **limit** | **int**| Number of items to return | [optional] [default to 10]
 **search** | **str**| Search filter for keys | [optional] 
 **include_values** | **bool**| Include values in the response. Secret values will be redacted as &#39;[ENCRYPTED]&#39; for security. | [optional] [default to False]

### Return type

[**V2StoreItemsListResponse**](V2StoreItemsListResponse.md)

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

# **k_v_items_show**
> KVItemsShow200Response k_v_items_show(organization, project, store_id, key)

Get an item from a kv store

Retrieves an item from the KV store. **Security Note:** If the item was stored as a secret (secret=true), the value will be redacted and returned as '[ENCRYPTED]' for security. Secrets should be accessed directly via the Quant Cloud platform KVStore abstraction.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.kv_items_show200_response import KVItemsShow200Response
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = '0000' # str | 
    key = 'key_example' # str | 

    try:
        # Get an item from a kv store
        api_response = api_instance.k_v_items_show(organization, project, store_id, key)
        print("The response of KVApi->k_v_items_show:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_items_show: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**|  | 
 **key** | **str**|  | 

### Return type

[**KVItemsShow200Response**](KVItemsShow200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The request has succeeded. |  -  |
**404** | Item not found. |  -  |
**403** | Access is forbidden. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_items_update**
> KVItemsCreate200Response k_v_items_update(organization, project, store_id, key, v2_store_item_update_request)

Update an item in a kv store

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.kv_items_create200_response import KVItemsCreate200Response
from quantcdn.models.v2_store_item_update_request import V2StoreItemUpdateRequest
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = '0000' # str | 
    key = 'key_example' # str | 
    v2_store_item_update_request = quantcdn.V2StoreItemUpdateRequest() # V2StoreItemUpdateRequest | 

    try:
        # Update an item in a kv store
        api_response = api_instance.k_v_items_update(organization, project, store_id, key, v2_store_item_update_request)
        print("The response of KVApi->k_v_items_update:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_items_update: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**|  | 
 **key** | **str**|  | 
 **v2_store_item_update_request** | [**V2StoreItemUpdateRequest**](V2StoreItemUpdateRequest.md)|  | 

### Return type

[**KVItemsCreate200Response**](KVItemsCreate200Response.md)

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
**422** | Validation error. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_list**
> List[V2Store] k_v_list(organization, project)

List key-value stores

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_store import V2Store
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier

    try:
        # List key-value stores
        api_response = api_instance.k_v_list(organization, project)
        print("The response of KVApi->k_v_list:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_list: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 

### Return type

[**List[V2Store]**](V2Store.md)

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

# **k_v_show**
> V2Store k_v_show(organization, project, store_id)

Get a kv store

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_store import V2Store
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = '0000' # str | 

    try:
        # Get a kv store
        api_response = api_instance.k_v_show(organization, project, store_id)
        print("The response of KVApi->k_v_show:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_show: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**|  | 

### Return type

[**V2Store**](V2Store.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The request has succeeded. |  -  |
**404** | KV store not found. |  -  |
**403** | Access is forbidden. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

