# quantcdn.BackupManagementApi

All URIs are relative to *https://dashboard.quantcdn.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_backup**](BackupManagementApi.md#create_backup) | **POST** /api/v3/organizations/{organisation}/applications/{application}/environments/{environment}/backups/{type} | Create a backup for an environment
[**delete_backup**](BackupManagementApi.md#delete_backup) | **DELETE** /api/v3/organizations/{organisation}/applications/{application}/environments/{environment}/backups/{type}/{backupId} | Delete a backup
[**download_backup**](BackupManagementApi.md#download_backup) | **GET** /api/v3/organizations/{organisation}/applications/{application}/environments/{environment}/backups/{type}/{backupId}/download | Generate a download URL for a backup
[**list_backups**](BackupManagementApi.md#list_backups) | **GET** /api/v3/organizations/{organisation}/applications/{application}/environments/{environment}/backups/{type} | List backups for an environment


# **create_backup**
> CreateBackup202Response create_backup(organisation, application, environment, type, create_backup_request=create_backup_request)

Create a backup for an environment

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.create_backup202_response import CreateBackup202Response
from quantcdn.models.create_backup_request import CreateBackupRequest
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
    api_instance = quantcdn.BackupManagementApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    application = 'application_example' # str | The application ID
    environment = 'environment_example' # str | The environment ID
    type = 'type_example' # str | The backup type
    create_backup_request = quantcdn.CreateBackupRequest() # CreateBackupRequest |  (optional)

    try:
        # Create a backup for an environment
        api_response = api_instance.create_backup(organisation, application, environment, type, create_backup_request=create_backup_request)
        print("The response of BackupManagementApi->create_backup:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BackupManagementApi->create_backup: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **application** | **str**| The application ID | 
 **environment** | **str**| The environment ID | 
 **type** | **str**| The backup type | 
 **create_backup_request** | [**CreateBackupRequest**](CreateBackupRequest.md)|  | [optional] 

### Return type

[**CreateBackup202Response**](CreateBackup202Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**202** | Backup operation initiated |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_backup**
> DeleteBackup200Response delete_backup(organisation, application, environment, type, backup_id)

Delete a backup

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.delete_backup200_response import DeleteBackup200Response
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
    api_instance = quantcdn.BackupManagementApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    application = 'application_example' # str | The application ID
    environment = 'environment_example' # str | The environment ID
    type = 'type_example' # str | The backup type
    backup_id = 'backup_id_example' # str | The backup ID

    try:
        # Delete a backup
        api_response = api_instance.delete_backup(organisation, application, environment, type, backup_id)
        print("The response of BackupManagementApi->delete_backup:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BackupManagementApi->delete_backup: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **application** | **str**| The application ID | 
 **environment** | **str**| The environment ID | 
 **type** | **str**| The backup type | 
 **backup_id** | **str**| The backup ID | 

### Return type

[**DeleteBackup200Response**](DeleteBackup200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Backup deleted successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **download_backup**
> DownloadBackup200Response download_backup(organisation, application, environment, type, backup_id)

Generate a download URL for a backup

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.download_backup200_response import DownloadBackup200Response
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
    api_instance = quantcdn.BackupManagementApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    application = 'application_example' # str | The application ID
    environment = 'environment_example' # str | The environment ID
    type = 'type_example' # str | The backup type
    backup_id = 'backup_id_example' # str | The backup ID

    try:
        # Generate a download URL for a backup
        api_response = api_instance.download_backup(organisation, application, environment, type, backup_id)
        print("The response of BackupManagementApi->download_backup:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BackupManagementApi->download_backup: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **application** | **str**| The application ID | 
 **environment** | **str**| The environment ID | 
 **type** | **str**| The backup type | 
 **backup_id** | **str**| The backup ID | 

### Return type

[**DownloadBackup200Response**](DownloadBackup200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Download URL generated successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_backups**
> ListBackups200Response list_backups(organisation, application, environment, type, order=order, limit=limit, created_before=created_before, created_after=created_after, status=status, next_token=next_token)

List backups for an environment

Retrieves a list of backups (database or filesystem) for the environment with status, size, and metadata. Supports filtering and ordering via query parameters.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.list_backups200_response import ListBackups200Response
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
    api_instance = quantcdn.BackupManagementApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    application = 'application_example' # str | The application ID
    environment = 'environment_example' # str | The environment ID
    type = 'type_example' # str | The backup type
    order = desc # str | Sort order for backups by creation date (asc = oldest first, desc = newest first) (optional) (default to desc)
    limit = 50 # int | Maximum number of backups to return (max 100) (optional) (default to 50)
    created_before = '2013-10-20T19:20:30+01:00' # datetime | Only return backups created before this ISO 8601 timestamp (e.g., 2025-01-01T00:00:00Z) (optional)
    created_after = '2013-10-20T19:20:30+01:00' # datetime | Only return backups created after this ISO 8601 timestamp (e.g., 2024-12-01T00:00:00Z) (optional)
    status = 'status_example' # str | Filter backups by status (optional)
    next_token = 'next_token_example' # str | Token for retrieving the next page of results (optional)

    try:
        # List backups for an environment
        api_response = api_instance.list_backups(organisation, application, environment, type, order=order, limit=limit, created_before=created_before, created_after=created_after, status=status, next_token=next_token)
        print("The response of BackupManagementApi->list_backups:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BackupManagementApi->list_backups: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **application** | **str**| The application ID | 
 **environment** | **str**| The environment ID | 
 **type** | **str**| The backup type | 
 **order** | **str**| Sort order for backups by creation date (asc &#x3D; oldest first, desc &#x3D; newest first) | [optional] [default to desc]
 **limit** | **int**| Maximum number of backups to return (max 100) | [optional] [default to 50]
 **created_before** | **datetime**| Only return backups created before this ISO 8601 timestamp (e.g., 2025-01-01T00:00:00Z) | [optional] 
 **created_after** | **datetime**| Only return backups created after this ISO 8601 timestamp (e.g., 2024-12-01T00:00:00Z) | [optional] 
 **status** | **str**| Filter backups by status | [optional] 
 **next_token** | **str**| Token for retrieving the next page of results | [optional] 

### Return type

[**ListBackups200Response**](ListBackups200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | List of backups |  -  |
**422** | Invalid backup type |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

