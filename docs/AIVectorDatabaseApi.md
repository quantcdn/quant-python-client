# quantcdn.AIVectorDatabaseApi

All URIs are relative to *https://dashboard.quantcdn.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_vector_collection**](AIVectorDatabaseApi.md#create_vector_collection) | **POST** /api/v3/organizations/{organisation}/ai/vector-db/collections | Create Vector Database Collection
[**delete_vector_collection**](AIVectorDatabaseApi.md#delete_vector_collection) | **DELETE** /api/v3/organizations/{organisation}/ai/vector-db/collections/{collectionId} | Delete Collection
[**get_vector_collection**](AIVectorDatabaseApi.md#get_vector_collection) | **GET** /api/v3/organizations/{organisation}/ai/vector-db/collections/{collectionId} | Get Collection Details
[**list_vector_collections**](AIVectorDatabaseApi.md#list_vector_collections) | **GET** /api/v3/organizations/{organisation}/ai/vector-db/collections | List Vector Database Collections
[**query_vector_collection**](AIVectorDatabaseApi.md#query_vector_collection) | **POST** /api/v3/organizations/{organisation}/ai/vector-db/collections/{collectionId}/query | Semantic Search Query
[**upload_vector_documents**](AIVectorDatabaseApi.md#upload_vector_documents) | **POST** /api/v3/organizations/{organisation}/ai/vector-db/collections/{collectionId}/documents | Upload Documents to Collection


# **create_vector_collection**
> CreateVectorCollection201Response create_vector_collection(organisation, create_vector_collection_request)

Create Vector Database Collection

Creates a new vector database collection (knowledge base category) for semantic search. Collections store documents with embeddings for RAG (Retrieval Augmented Generation).
     *
     * **Use Cases:**
     * - Product documentation ('docs')
     * - Company policies ('policies')
     * - Support knowledge base ('support')
     * - Technical specifications ('specs')

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.create_vector_collection201_response import CreateVectorCollection201Response
from quantcdn.models.create_vector_collection_request import CreateVectorCollectionRequest
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
    api_instance = quantcdn.AIVectorDatabaseApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    create_vector_collection_request = quantcdn.CreateVectorCollectionRequest() # CreateVectorCollectionRequest | 

    try:
        # Create Vector Database Collection
        api_response = api_instance.create_vector_collection(organisation, create_vector_collection_request)
        print("The response of AIVectorDatabaseApi->create_vector_collection:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIVectorDatabaseApi->create_vector_collection: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **create_vector_collection_request** | [**CreateVectorCollectionRequest**](CreateVectorCollectionRequest.md)|  | 

### Return type

[**CreateVectorCollection201Response**](CreateVectorCollection201Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Collection created successfully |  -  |
**400** | Invalid request parameters |  -  |
**403** | Access denied |  -  |
**409** | Collection with this name already exists |  -  |
**500** | Failed to create collection |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_vector_collection**
> DeleteVectorCollection200Response delete_vector_collection(organisation, collection_id)

Delete Collection

Deletes a vector database collection and all its documents. This action cannot be undone.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.delete_vector_collection200_response import DeleteVectorCollection200Response
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
    api_instance = quantcdn.AIVectorDatabaseApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    collection_id = 'collection_id_example' # str | The collection ID

    try:
        # Delete Collection
        api_response = api_instance.delete_vector_collection(organisation, collection_id)
        print("The response of AIVectorDatabaseApi->delete_vector_collection:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIVectorDatabaseApi->delete_vector_collection: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **collection_id** | **str**| The collection ID | 

### Return type

[**DeleteVectorCollection200Response**](DeleteVectorCollection200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Collection deleted successfully |  -  |
**403** | Access denied |  -  |
**404** | Collection not found |  -  |
**500** | Failed to delete collection |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_vector_collection**
> GetVectorCollection200Response get_vector_collection(organisation, collection_id)

Get Collection Details

Get detailed information about a specific vector database collection.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.get_vector_collection200_response import GetVectorCollection200Response
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
    api_instance = quantcdn.AIVectorDatabaseApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    collection_id = 'collection_id_example' # str | The collection ID

    try:
        # Get Collection Details
        api_response = api_instance.get_vector_collection(organisation, collection_id)
        print("The response of AIVectorDatabaseApi->get_vector_collection:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIVectorDatabaseApi->get_vector_collection: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **collection_id** | **str**| The collection ID | 

### Return type

[**GetVectorCollection200Response**](GetVectorCollection200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Collection details retrieved successfully |  -  |
**403** | Access denied |  -  |
**404** | Collection not found |  -  |
**500** | Failed to retrieve collection |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_vector_collections**
> ListVectorCollections200Response list_vector_collections(organisation)

List Vector Database Collections

Lists all vector database collections (knowledge bases) for an organization.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.list_vector_collections200_response import ListVectorCollections200Response
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
    api_instance = quantcdn.AIVectorDatabaseApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID

    try:
        # List Vector Database Collections
        api_response = api_instance.list_vector_collections(organisation)
        print("The response of AIVectorDatabaseApi->list_vector_collections:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIVectorDatabaseApi->list_vector_collections: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 

### Return type

[**ListVectorCollections200Response**](ListVectorCollections200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Collections retrieved successfully |  -  |
**403** | Access denied |  -  |
**500** | Failed to retrieve collections |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **query_vector_collection**
> QueryVectorCollection200Response query_vector_collection(organisation, collection_id, query_vector_collection_request)

Semantic Search Query

Performs semantic search on a collection using vector similarity. Returns the most relevant documents based on meaning, not keyword matching.
     *
     * **Use Cases:**
     * - Find relevant documentation for user questions
     * - Power RAG (Retrieval Augmented Generation) in AI assistants
     * - Semantic search across knowledge bases

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.query_vector_collection200_response import QueryVectorCollection200Response
from quantcdn.models.query_vector_collection_request import QueryVectorCollectionRequest
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
    api_instance = quantcdn.AIVectorDatabaseApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    collection_id = 'collection_id_example' # str | The collection ID
    query_vector_collection_request = quantcdn.QueryVectorCollectionRequest() # QueryVectorCollectionRequest | 

    try:
        # Semantic Search Query
        api_response = api_instance.query_vector_collection(organisation, collection_id, query_vector_collection_request)
        print("The response of AIVectorDatabaseApi->query_vector_collection:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIVectorDatabaseApi->query_vector_collection: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **collection_id** | **str**| The collection ID | 
 **query_vector_collection_request** | [**QueryVectorCollectionRequest**](QueryVectorCollectionRequest.md)|  | 

### Return type

[**QueryVectorCollection200Response**](QueryVectorCollection200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Search completed successfully |  -  |
**400** | Invalid request parameters |  -  |
**403** | Access denied |  -  |
**404** | Collection not found |  -  |
**500** | Failed to perform search |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **upload_vector_documents**
> UploadVectorDocuments200Response upload_vector_documents(organisation, collection_id, upload_vector_documents_request)

Upload Documents to Collection

Uploads documents to a vector database collection with automatic embedding generation. Documents are chunked (if needed), embedded using the collection's embedding model, and stored.
     *
     * **Supported Content:**
     * - Plain text content
     * - URLs to fetch content from
     * - Markdown documents
     *
     * **Metadata:**
     * Each document can include metadata (title, source_url, section, tags) that is returned with search results.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.upload_vector_documents200_response import UploadVectorDocuments200Response
from quantcdn.models.upload_vector_documents_request import UploadVectorDocumentsRequest
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
    api_instance = quantcdn.AIVectorDatabaseApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    collection_id = 'collection_id_example' # str | The collection ID
    upload_vector_documents_request = quantcdn.UploadVectorDocumentsRequest() # UploadVectorDocumentsRequest | 

    try:
        # Upload Documents to Collection
        api_response = api_instance.upload_vector_documents(organisation, collection_id, upload_vector_documents_request)
        print("The response of AIVectorDatabaseApi->upload_vector_documents:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIVectorDatabaseApi->upload_vector_documents: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **collection_id** | **str**| The collection ID | 
 **upload_vector_documents_request** | [**UploadVectorDocumentsRequest**](UploadVectorDocumentsRequest.md)|  | 

### Return type

[**UploadVectorDocuments200Response**](UploadVectorDocuments200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Documents uploaded successfully |  -  |
**400** | Invalid request parameters |  -  |
**403** | Access denied |  -  |
**404** | Collection not found |  -  |
**500** | Failed to upload documents |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

