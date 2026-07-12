# quantcdn.RestoreManagementApi

All URIs are relative to *https://dashboard.quantcdn.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_restore_status**](RestoreManagementApi.md#get_restore_status) | **GET** /api/v3/organizations/{organisation}/applications/{application}/environments/{environment}/restores/{restoreId} | Get the status of a restore operation
[**restore_database**](RestoreManagementApi.md#restore_database) | **POST** /api/v3/organizations/{organisation}/applications/{application}/environments/{environment}/backups/{backupId}/restore-database | Restore a database backup to a target environment
[**restore_filesystem**](RestoreManagementApi.md#restore_filesystem) | **POST** /api/v3/organizations/{organisation}/applications/{application}/environments/{environment}/backups/{backupId}/restore-filesystem | Restore a filesystem backup to a target environment


# **get_restore_status**
> GetRestoreStatus200Response get_restore_status(organisation, application, environment, restore_id)

Get the status of a restore operation

Returns the current status and metadata for a restore operation. Poll this endpoint to track progress.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.get_restore_status200_response import GetRestoreStatus200Response
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
    api_instance = quantcdn.RestoreManagementApi(api_client)
    organisation = 'test-org' # str | The organisation ID
    application = 'test-app' # str | The application ID
    environment = 'staging' # str | The environment ID
    restore_id = 'restore-abc123' # str | The restore operation ID

    try:
        # Get the status of a restore operation
        api_response = api_instance.get_restore_status(organisation, application, environment, restore_id)
        print("The response of RestoreManagementApi->get_restore_status:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RestoreManagementApi->get_restore_status: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **application** | **str**| The application ID | 
 **environment** | **str**| The environment ID | 
 **restore_id** | **str**| The restore operation ID | 

### Return type

[**GetRestoreStatus200Response**](GetRestoreStatus200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Restore operation record |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **restore_database**
> RestoreDatabase202Response restore_database(organisation, application, environment, backup_id, restore_database_request)

Restore a database backup to a target environment

Initiates an async restore of a database backup into the specified target environment. The backup may originate from a different environment of the same application (cross-env restore). Returns 202 with a restoreId for status polling.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.restore_database202_response import RestoreDatabase202Response
from quantcdn.models.restore_database_request import RestoreDatabaseRequest
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
    api_instance = quantcdn.RestoreManagementApi(api_client)
    organisation = 'test-org' # str | The organisation ID
    application = 'test-app' # str | The application ID
    environment = 'staging' # str | The TARGET environment ID to restore INTO
    backup_id = 'quant-gov-dashboard-staging-2025-09-19T21-50-27-145Z' # str | The backup ID to restore from
    restore_database_request = quantcdn.RestoreDatabaseRequest() # RestoreDatabaseRequest | 

    try:
        # Restore a database backup to a target environment
        api_response = api_instance.restore_database(organisation, application, environment, backup_id, restore_database_request)
        print("The response of RestoreManagementApi->restore_database:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RestoreManagementApi->restore_database: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **application** | **str**| The application ID | 
 **environment** | **str**| The TARGET environment ID to restore INTO | 
 **backup_id** | **str**| The backup ID to restore from | 
 **restore_database_request** | [**RestoreDatabaseRequest**](RestoreDatabaseRequest.md)|  | 

### Return type

[**RestoreDatabase202Response**](RestoreDatabase202Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**202** | Restore operation initiated |  -  |
**422** | Validation error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **restore_filesystem**
> RestoreFilesystem202Response restore_filesystem(organisation, application, environment, backup_id, restore_filesystem_request)

Restore a filesystem backup to a target environment

Initiates an async restore of a filesystem backup into the specified target environment. The backup may originate from a different environment of the same application (cross-env restore). Returns 202 with a restoreId for status polling.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.restore_filesystem202_response import RestoreFilesystem202Response
from quantcdn.models.restore_filesystem_request import RestoreFilesystemRequest
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
    api_instance = quantcdn.RestoreManagementApi(api_client)
    organisation = 'test-org' # str | The organisation ID
    application = 'test-app' # str | The application ID
    environment = 'staging' # str | The TARGET environment ID to restore INTO
    backup_id = 'quant-gov-dashboard-staging-2025-09-19T21-50-27-145Z' # str | The backup ID to restore from
    restore_filesystem_request = quantcdn.RestoreFilesystemRequest() # RestoreFilesystemRequest | 

    try:
        # Restore a filesystem backup to a target environment
        api_response = api_instance.restore_filesystem(organisation, application, environment, backup_id, restore_filesystem_request)
        print("The response of RestoreManagementApi->restore_filesystem:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RestoreManagementApi->restore_filesystem: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **application** | **str**| The application ID | 
 **environment** | **str**| The TARGET environment ID to restore INTO | 
 **backup_id** | **str**| The backup ID to restore from | 
 **restore_filesystem_request** | [**RestoreFilesystemRequest**](RestoreFilesystemRequest.md)|  | 

### Return type

[**RestoreFilesystem202Response**](RestoreFilesystem202Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**202** | Restore operation initiated |  -  |
**422** | Validation error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

