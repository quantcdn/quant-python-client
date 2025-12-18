# V1FormSubmissionListResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**draw** | **int** |  | 
**i_total_records** | **int** |  | 
**i_total_display_records** | **int** |  | 
**aa_data** | [**List[V1FormSubmissionItem]**](V1FormSubmissionItem.md) |  | 

## Example

```python
from quantcdn.models.v1_form_submission_list_response import V1FormSubmissionListResponse

# TODO update the JSON string below
json = "{}"
# create an instance of V1FormSubmissionListResponse from a JSON string
v1_form_submission_list_response_instance = V1FormSubmissionListResponse.from_json(json)
# print the JSON string representation of the object
print(V1FormSubmissionListResponse.to_json())

# convert the object into a dict
v1_form_submission_list_response_dict = v1_form_submission_list_response_instance.to_dict()
# create an instance of V1FormSubmissionListResponse from a dict
v1_form_submission_list_response_from_dict = V1FormSubmissionListResponse.from_dict(v1_form_submission_list_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


