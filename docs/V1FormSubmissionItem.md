# V1FormSubmissionItem


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uuid** | **str** |  | 
**country_ip** | **str** |  | 
**spam_score** | **str** |  | 
**data** | **str** |  | 
**file_count** | **int** |  | 
**date_submitted** | **str** |  | 

## Example

```python
from quantcdn.models.v1_form_submission_item import V1FormSubmissionItem

# TODO update the JSON string below
json = "{}"
# create an instance of V1FormSubmissionItem from a JSON string
v1_form_submission_item_instance = V1FormSubmissionItem.from_json(json)
# print the JSON string representation of the object
print(V1FormSubmissionItem.to_json())

# convert the object into a dict
v1_form_submission_item_dict = v1_form_submission_item_instance.to_dict()
# create an instance of V1FormSubmissionItem from a dict
v1_form_submission_item_from_dict = V1FormSubmissionItem.from_dict(v1_form_submission_item_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


