# quantcdn.AlertChannelsApi

All URIs are relative to *https://dashboard.quantcdn.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**alert_channels_list**](AlertChannelsApi.md#alert_channels_list) | **GET** /api/v3/organizations/{organisation}/projects/{project}/alert-channels | List the organisation&#39;s alert channels


# **alert_channels_list**
> AlertChannelList alert_channels_list(organisation, project)

List the organisation's alert channels

Returns every alert channel of the organisation (channels are organisation-wide; the project segment lets a project-limited token call it). Each item has the ID, name, type and a masked hint only. Needs the alert-channels:read scope and the view_alert_channels permission.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.alert_channel_list import AlertChannelList
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
    api_instance = quantcdn.AlertChannelsApi(api_client)
    organisation = 'test-org' # str | The organisation machine name
    project = 'test-project' # str | The project machine name

    try:
        # List the organisation's alert channels
        api_response = api_instance.alert_channels_list(organisation, project)
        print("The response of AlertChannelsApi->alert_channels_list:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AlertChannelsApi->alert_channels_list: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation machine name | 
 **project** | **str**| The project machine name | 

### Return type

[**AlertChannelList**](AlertChannelList.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The organisation&#39;s alert channels |  -  |
**401** | Unauthorized |  -  |
**403** | The token or role cannot read alert channels, or the token is limited to another project |  -  |
**404** | Alert channels are not available on this platform |  -  |
**502** | The alerts service did not answer |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

