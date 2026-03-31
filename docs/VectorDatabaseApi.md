# quantcdn.VectorDatabaseApi

All URIs are relative to *https://dashboard.quantcdn.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**list_vector_documents**](VectorDatabaseApi.md#list_vector_documents) | **GET** /api/v3/organizations/{organisation}/ai/vector-db/collections/{collectionId}/documents | List Documents in Collection


# **list_vector_documents**
> list_vector_documents(organisation, collection_id, key=key, limit=limit, offset=offset)

List Documents in Collection

Lists documents in a collection with pagination. Supports filtering by document key.

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
    api_instance = quantcdn.VectorDatabaseApi(api_client)
    organisation = 'organisation_example' # str | 
    collection_id = 'collection_id_example' # str | 
    key = 'key_example' # str | Filter by document key (optional)
    limit = 50 # int |  (optional) (default to 50)
    offset = 0 # int |  (optional) (default to 0)

    try:
        # List Documents in Collection
        api_instance.list_vector_documents(organisation, collection_id, key=key, limit=limit, offset=offset)
    except Exception as e:
        print("Exception when calling VectorDatabaseApi->list_vector_documents: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**|  | 
 **collection_id** | **str**|  | 
 **key** | **str**| Filter by document key | [optional] 
 **limit** | **int**|  | [optional] [default to 50]
 **offset** | **int**|  | [optional] [default to 0]

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
**200** | Documents retrieved successfully |  -  |
**403** | Access denied |  -  |
**404** | Collection not found |  -  |
**500** | Failed to list documents |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

