# quantcdn.AIFileStorageApi

All URIs are relative to *https://dashboard.quantcdn.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_file**](AIFileStorageApi.md#delete_file) | **DELETE** /api/v3/organizations/{organisation}/ai/files/{fileId} | Delete File
[**get_file**](AIFileStorageApi.md#get_file) | **GET** /api/v3/organizations/{organisation}/ai/files/{fileId} | Get File
[**list_files**](AIFileStorageApi.md#list_files) | **GET** /api/v3/organizations/{organisation}/ai/files | List Files
[**upload_file**](AIFileStorageApi.md#upload_file) | **POST** /api/v3/organizations/{organisation}/ai/files | Upload File to S3


# **delete_file**
> DeleteFile200Response delete_file(organisation, file_id)

Delete File

Deletes a file from S3 storage.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.delete_file200_response import DeleteFile200Response
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
    api_instance = quantcdn.AIFileStorageApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    file_id = 'file_id_example' # str | The file ID

    try:
        # Delete File
        api_response = api_instance.delete_file(organisation, file_id)
        print("The response of AIFileStorageApi->delete_file:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIFileStorageApi->delete_file: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **file_id** | **str**| The file ID | 

### Return type

[**DeleteFile200Response**](DeleteFile200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | File deleted successfully |  -  |
**403** | Access denied |  -  |
**404** | File not found |  -  |
**500** | Failed to delete file |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_file**
> GetFile200Response get_file(organisation, file_id)

Get File

Retrieves file metadata and a presigned download URL (valid for 1 hour).

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.get_file200_response import GetFile200Response
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
    api_instance = quantcdn.AIFileStorageApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    file_id = 'file_id_example' # str | The file ID

    try:
        # Get File
        api_response = api_instance.get_file(organisation, file_id)
        print("The response of AIFileStorageApi->get_file:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIFileStorageApi->get_file: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **file_id** | **str**| The file ID | 

### Return type

[**GetFile200Response**](GetFile200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | File metadata and download URL |  -  |
**403** | Access denied |  -  |
**404** | File not found |  -  |
**500** | Failed to get file |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_files**
> ListFiles200Response list_files(organisation, filter=filter, limit=limit, cursor=cursor)

List Files

Lists files stored in S3 for this organization with optional metadata filtering and pagination.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.list_files200_response import ListFiles200Response
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
    api_instance = quantcdn.AIFileStorageApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    filter = '{}' # str | JSON-encoded metadata filter. Supports exact match and array contains filters. (optional)
    limit = 50 # int | Maximum files to return (optional) (default to 50)
    cursor = 'cursor_example' # str | Pagination cursor from previous response (optional)

    try:
        # List Files
        api_response = api_instance.list_files(organisation, filter=filter, limit=limit, cursor=cursor)
        print("The response of AIFileStorageApi->list_files:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIFileStorageApi->list_files: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **filter** | **str**| JSON-encoded metadata filter. Supports exact match and array contains filters. | [optional] 
 **limit** | **int**| Maximum files to return | [optional] [default to 50]
 **cursor** | **str**| Pagination cursor from previous response | [optional] 

### Return type

[**ListFiles200Response**](ListFiles200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | List of files |  -  |
**400** | Invalid filter parameter |  -  |
**403** | Access denied |  -  |
**500** | Failed to list files |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **upload_file**
> UploadFile201Response upload_file(organisation, upload_file_request)

Upload File to S3

Uploads a file to S3 storage for later retrieval.
     *
     * **Two Upload Modes:**
     *
     * 1. **Direct Upload (≤7MB):** Send base64-encoded content in request body.
     *
     * 2. **Presigned URL Upload (any size):** Set `requestUploadUrl: true` to get a presigned S3 PUT URL, then upload directly to S3.
     *
     * **Supported Content Types:**
     * - Images: image/png, image/jpeg, image/gif, image/webp, image/svg+xml
     * - Documents: application/pdf, text/plain, text/markdown, text/html
     * - Code: text/javascript, application/json, text/css, text/yaml
     * - Archives: application/zip, application/gzip
     * - Video: video/mp4, video/webm (use presigned URL for large files)
     *
     * **Metadata:**
     * Attach any custom metadata for filtering. `artifactType` is auto-populated from contentType if not provided.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.upload_file201_response import UploadFile201Response
from quantcdn.models.upload_file_request import UploadFileRequest
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
    api_instance = quantcdn.AIFileStorageApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    upload_file_request = quantcdn.UploadFileRequest() # UploadFileRequest | 

    try:
        # Upload File to S3
        api_response = api_instance.upload_file(organisation, upload_file_request)
        print("The response of AIFileStorageApi->upload_file:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIFileStorageApi->upload_file: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **upload_file_request** | [**UploadFileRequest**](UploadFileRequest.md)|  | 

### Return type

[**UploadFile201Response**](UploadFile201Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | File uploaded or presigned URL generated |  -  |
**400** | Invalid request parameters |  -  |
**403** | Access denied |  -  |
**413** | File too large (use requestUploadUrl for large files) |  -  |
**500** | Failed to upload file |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

