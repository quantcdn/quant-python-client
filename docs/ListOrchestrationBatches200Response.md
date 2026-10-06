# ListOrchestrationBatches200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**batches** | [**List[ListOrchestrationBatches200ResponseBatchesInner]**](ListOrchestrationBatches200ResponseBatchesInner.md) |  | [optional] 
**next_cursor** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.list_orchestration_batches200_response import ListOrchestrationBatches200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ListOrchestrationBatches200Response from a JSON string
list_orchestration_batches200_response_instance = ListOrchestrationBatches200Response.from_json(json)
# print the JSON string representation of the object
print(ListOrchestrationBatches200Response.to_json())

# convert the object into a dict
list_orchestration_batches200_response_dict = list_orchestration_batches200_response_instance.to_dict()
# create an instance of ListOrchestrationBatches200Response from a dict
list_orchestration_batches200_response_from_dict = ListOrchestrationBatches200Response.from_dict(list_orchestration_batches200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


