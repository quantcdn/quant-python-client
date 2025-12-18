# V2RuleProxyAction


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**to** | **str** | Target URL to proxy to | 
**host** | **str** | Host header override | [optional] 
**auth_user** | **str** | Basic auth username | [optional] 
**auth_pass** | **str** | Basic auth password | [optional] 
**disable_ssl_verify** | **bool** | Disable SSL verification | [optional] [default to False]
**cache_lifetime** | **str** | Cache lifetime | [optional] 
**only_proxy_404** | **bool** | Only proxy 404 responses | [optional] [default to False]
**inject_headers** | **Dict[str, str]** | Headers to inject | [optional] 
**proxy_strip_headers** | **List[str]** | Headers to strip from response | [optional] 
**proxy_strip_request_headers** | **List[str]** | Headers to strip from request | [optional] 
**origin_timeout** | **str** | Origin timeout | [optional] 
**failover_mode** | **bool** | Enable failover mode | [optional] [default to False]
**failover_origin_ttfb** | **str** | Failover TTFB threshold | [optional] [default to '2000']
**failover_origin_status_codes** | **List[str]** | Status codes for failover (default: 200,404,301,302,304) | [optional] 
**failover_lifetime** | **str** | Failover cache lifetime | [optional] [default to '300']
**notify** | **str** | Notification type (none, slack) | [optional] [default to 'none']
**notify_config** | [**V2RuleProxyActionNotifyConfig**](V2RuleProxyActionNotifyConfig.md) |  | [optional] 
**waf_enabled** | **bool** | WAF enabled | [optional] [default to False]
**waf_config** | [**WafConfig**](WafConfig.md) |  | [optional] 
**proxy_alert_enabled** | **bool** | Proxy alert enabled | [optional] 
**proxy_inline_fn_enabled** | **bool** | Proxy inline function enabled | [optional] [default to False]
**application_proxy** | **bool** | Enable Quant Cloud application proxy mode | [optional] [default to False]
**application_name** | **str** | Quant Cloud application name (required when application_proxy is true) | [optional] 
**application_environment** | **str** | Quant Cloud application environment (required when application_proxy is true) | [optional] 
**application_container** | **str** | Quant Cloud application container (required when application_proxy is true) | [optional] 
**application_port** | **int** | Quant Cloud application port (required when application_proxy is true) | [optional] 
**quant_cloud_selection** | [**V2RuleProxyActionQuantCloudSelection**](V2RuleProxyActionQuantCloudSelection.md) |  | [optional] 
**static_error_page** | **str** | Static error page content (HTML) to serve on origin errors | [optional] 
**static_error_page_status_codes** | **List[str]** | Origin status codes that trigger static error page | [optional] 

## Example

```python
from quantcdn.models.v2_rule_proxy_action import V2RuleProxyAction

# TODO update the JSON string below
json = "{}"
# create an instance of V2RuleProxyAction from a JSON string
v2_rule_proxy_action_instance = V2RuleProxyAction.from_json(json)
# print the JSON string representation of the object
print(V2RuleProxyAction.to_json())

# convert the object into a dict
v2_rule_proxy_action_dict = v2_rule_proxy_action_instance.to_dict()
# create an instance of V2RuleProxyAction from a dict
v2_rule_proxy_action_from_dict = V2RuleProxyAction.from_dict(v2_rule_proxy_action_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


