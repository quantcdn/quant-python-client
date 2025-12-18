# quantcdn.AIInferenceApi

All URIs are relative to *https://dashboard.quantcdn.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**chat_inference**](AIInferenceApi.md#chat_inference) | **POST** /api/v3/organizations/{organisation}/ai/chat | Chat inference via API Gateway (buffered responses) with multimodal support
[**chat_inference_stream**](AIInferenceApi.md#chat_inference_stream) | **POST** /api/v3/organizations/{organisation}/ai/chat/stream | Chat inference via streaming endpoint (true HTTP streaming) with multimodal support
[**embeddings**](AIInferenceApi.md#embeddings) | **POST** /api/v3/organizations/{organisation}/ai/embeddings | Generate text embeddings for semantic search and RAG applications
[**image_generation**](AIInferenceApi.md#image_generation) | **POST** /api/v3/organizations/{organisation}/ai/image-generation | Generate images with Amazon Nova Canvas


# **chat_inference**
> ChatInference200Response chat_inference(organisation, chat_inference_request)

Chat inference via API Gateway (buffered responses) with multimodal support

Sends requests to the AI API Gateway endpoint which buffers responses. Supports text, images, videos, and documents via base64 encoding.
     *
     * **Multimodal Support:**
     * - **Text**: Simple string content
     * - **Images**: Base64-encoded PNG, JPEG, GIF, WebP (up to 25MB)
     * - **Videos**: Base64-encoded MP4, MOV, WebM, etc. (up to 25MB)
     * - **Documents**: Base64-encoded PDF, DOCX, CSV, etc. (up to 25MB)
     *
     * **Supported Models:**
     * - Amazon Nova Lite, Micro, Pro (all support multimodal)
     * - Claude models (text only)
     *
     * **Usage Tips:**
     * - Use base64 encoding for images/videos < 5-10MB
     * - Place media before text prompts for best results
     * - Label multiple media files (e.g., 'Image 1:', 'Image 2:')
     * - Maximum 25MB total payload size
     *
     * **Response Patterns:**
     * - **Text-only**: Returns simple text response when no tools requested
     * - **Single tool**: Returns `toolUse` object when AI requests one tool
     * - **Multiple tools**: Returns `toolUse` array when AI requests multiple tools
     * - **Auto-execute sync**: Automatically executes tool and returns final text response
     * - **Auto-execute async**: Returns toolUse with `executionId` and `status` for polling

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.chat_inference200_response import ChatInference200Response
from quantcdn.models.chat_inference_request import ChatInferenceRequest
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
    api_instance = quantcdn.AIInferenceApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    chat_inference_request = quantcdn.ChatInferenceRequest() # ChatInferenceRequest | Chat request with optional multimodal content blocks

    try:
        # Chat inference via API Gateway (buffered responses) with multimodal support
        api_response = api_instance.chat_inference(organisation, chat_inference_request)
        print("The response of AIInferenceApi->chat_inference:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIInferenceApi->chat_inference: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **chat_inference_request** | [**ChatInferenceRequest**](ChatInferenceRequest.md)| Chat request with optional multimodal content blocks | 

### Return type

[**ChatInference200Response**](ChatInference200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Chat inference completed (buffered response) |  -  |
**500** | Failed to perform chat inference |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **chat_inference_stream**
> str chat_inference_stream(organisation, chat_inference_stream_request)

Chat inference via streaming endpoint (true HTTP streaming) with multimodal support

Streams responses from the AI streaming subdomain using Server-Sent Events (SSE). Tokens are streamed in real-time as they are generated.
     *
     * **Multimodal Support:**
     * - **Text**: Simple string content
     * - **Images**: Base64-encoded PNG, JPEG, GIF, WebP (up to 25MB)
     * - **Videos**: Base64-encoded MP4, MOV, WebM, etc. (up to 25MB)
     * - **Documents**: Base64-encoded PDF, DOCX, CSV, etc. (up to 25MB)
     *
     * **Supported Models:**
     * - Amazon Nova Lite, Micro, Pro (all support multimodal)
     * - Claude models (text only)
     *
     * **Usage Tips:**
     * - Use base64 encoding for images/videos < 5-10MB
     * - Place media before text prompts for best results
     * - Label multiple media files (e.g., 'Image 1:', 'Image 2:')
     * - Maximum 25MB total payload size
     * - Streaming works with all content types (text, image, video, document)

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.chat_inference_stream_request import ChatInferenceStreamRequest
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
    api_instance = quantcdn.AIInferenceApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    chat_inference_stream_request = quantcdn.ChatInferenceStreamRequest() # ChatInferenceStreamRequest | Chat request with optional multimodal content blocks

    try:
        # Chat inference via streaming endpoint (true HTTP streaming) with multimodal support
        api_response = api_instance.chat_inference_stream(organisation, chat_inference_stream_request)
        print("The response of AIInferenceApi->chat_inference_stream:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIInferenceApi->chat_inference_stream: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **chat_inference_stream_request** | [**ChatInferenceStreamRequest**](ChatInferenceStreamRequest.md)| Chat request with optional multimodal content blocks | 

### Return type

**str**

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: text/event-stream

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Streaming response (text/event-stream) |  -  |
**500** | Failed to perform streaming inference |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **embeddings**
> Embeddings200Response embeddings(organisation, embeddings_request)

Generate text embeddings for semantic search and RAG applications

Generates vector embeddings for text content using embedding models. Used for semantic search, document similarity, and RAG applications.
     *
     * **Features:**
     * - Single text or batch processing (up to 100 texts)
     * - Configurable dimensions (256, 512, 1024, 8192 for Titan v2)
     * - Optional normalization to unit length
     * - Usage tracking for billing
     *
     * **Use Cases:**
     * - Semantic search across documents
     * - Similarity matching for content recommendations
     * - RAG (Retrieval-Augmented Generation) pipelines
     * - Clustering and classification
     *
     * **Available Embedding Models:**
     * - amazon.titan-embed-text-v2:0 (default, supports 256-8192 dimensions)
     * - amazon.titan-embed-text-v1:0 (1536 dimensions fixed)

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.embeddings200_response import Embeddings200Response
from quantcdn.models.embeddings_request import EmbeddingsRequest
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
    api_instance = quantcdn.AIInferenceApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    embeddings_request = {"input":"The Australian government announced new climate policy","modelId":"amazon.titan-embed-text-v2:0","dimensions":1024,"normalize":true} # EmbeddingsRequest | Embedding request with single or multiple texts

    try:
        # Generate text embeddings for semantic search and RAG applications
        api_response = api_instance.embeddings(organisation, embeddings_request)
        print("The response of AIInferenceApi->embeddings:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIInferenceApi->embeddings: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **embeddings_request** | [**EmbeddingsRequest**](EmbeddingsRequest.md)| Embedding request with single or multiple texts | 

### Return type

[**Embeddings200Response**](Embeddings200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Embeddings generated successfully |  -  |
**400** | Invalid request parameters |  -  |
**403** | Access denied |  -  |
**500** | Failed to generate embeddings |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **image_generation**
> ImageGeneration200Response image_generation(organisation, image_generation_request)

Generate images with Amazon Nova Canvas

Generates images using Amazon Nova Canvas image generation model.
     *
     * **Region Restriction:** Nova Canvas is ONLY available in:
     * - `us-east-1` (US East, N. Virginia)
     * - `ap-northeast-1` (Asia Pacific, Tokyo)
     * - `eu-west-1` (Europe, Ireland)
     * ❌ NOT available in `ap-southeast-2` (Sydney)
     *
     * **Supported Task Types:**
     * - **TEXT_IMAGE**: Basic text-to-image generation
     * - **TEXT_IMAGE with Conditioning**: Layout-guided generation using edge detection or segmentation
     * - **COLOR_GUIDED_GENERATION**: Generate images with specific color palettes
     * - **IMAGE_VARIATION**: Create variations of existing images
     * - **INPAINTING**: Fill masked areas in images
     * - **OUTPAINTING**: Extend images beyond their borders
     * - **BACKGROUND_REMOVAL**: Remove backgrounds from images
     * - **VIRTUAL_TRY_ON**: Try on garments/objects on people
     *
     * **Quality Options:**
     * - **standard**: Faster generation, lower cost
     * - **premium**: Higher quality, slower generation
     *
     * **Timeout:** Image generation can take up to 5 minutes

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.image_generation200_response import ImageGeneration200Response
from quantcdn.models.image_generation_request import ImageGenerationRequest
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
    api_instance = quantcdn.AIInferenceApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    image_generation_request = {"taskType":"TEXT_IMAGE","textToImageParams":{"text":"A serene mountain landscape at sunset with snow-capped peaks","negativeText":"blurry, low quality, distorted","style":"PHOTOREALISM"},"imageGenerationConfig":{"width":1024,"height":1024,"quality":"premium","numberOfImages":1,"cfgScale":7},"region":"us-east-1"} # ImageGenerationRequest | Image generation request

    try:
        # Generate images with Amazon Nova Canvas
        api_response = api_instance.image_generation(organisation, image_generation_request)
        print("The response of AIInferenceApi->image_generation:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIInferenceApi->image_generation: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **image_generation_request** | [**ImageGenerationRequest**](ImageGenerationRequest.md)| Image generation request | 

### Return type

[**ImageGeneration200Response**](ImageGeneration200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Image(s) generated successfully |  -  |
**400** | Invalid request parameters |  -  |
**403** | Access denied |  -  |
**500** | Failed to generate images |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

