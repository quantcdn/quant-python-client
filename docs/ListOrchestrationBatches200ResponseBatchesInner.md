# ListOrchestrationBatches200ResponseBatchesInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**batch_id** | **str** |  | [optional] 
**orchestration_id** | **str** |  | [optional] 
**iteration** | **int** |  | [optional] 
**item_count** | **int** |  | [optional] 
**completed_count** | **int** |  | [optional] 
**failed_count** | **int** |  | [optional] 
**status** | **str** |  | [optional] 
**started_at** | **datetime** |  | [optional] 
**completed_at** | **datetime** |  | [optional] 
**error** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.list_orchestration_batches200_response_batches_inner import ListOrchestrationBatches200ResponseBatchesInner

# TODO update the JSON string below
json = "{}"
# create an instance of ListOrchestrationBatches200ResponseBatchesInner from a JSON string
list_orchestration_batches200_response_batches_inner_instance = ListOrchestrationBatches200ResponseBatchesInner.from_json(json)
# print the JSON string representation of the object
print(ListOrchestrationBatches200ResponseBatchesInner.to_json())

# convert the object into a dict
list_orchestration_batches200_response_batches_inner_dict = list_orchestration_batches200_response_batches_inner_instance.to_dict()
# create an instance of ListOrchestrationBatches200ResponseBatchesInner from a dict
list_orchestration_batches200_response_batches_inner_from_dict = ListOrchestrationBatches200ResponseBatchesInner.from_dict(list_orchestration_batches200_response_batches_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


