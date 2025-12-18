# ImageGenerationRequestBackgroundRemovalParams

Parameters for BACKGROUND_REMOVAL task

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**image** | **bytearray** |  | [optional] 

## Example

```python
from quantcdn.models.image_generation_request_background_removal_params import ImageGenerationRequestBackgroundRemovalParams

# TODO update the JSON string below
json = "{}"
# create an instance of ImageGenerationRequestBackgroundRemovalParams from a JSON string
image_generation_request_background_removal_params_instance = ImageGenerationRequestBackgroundRemovalParams.from_json(json)
# print the JSON string representation of the object
print(ImageGenerationRequestBackgroundRemovalParams.to_json())

# convert the object into a dict
image_generation_request_background_removal_params_dict = image_generation_request_background_removal_params_instance.to_dict()
# create an instance of ImageGenerationRequestBackgroundRemovalParams from a dict
image_generation_request_background_removal_params_from_dict = ImageGenerationRequestBackgroundRemovalParams.from_dict(image_generation_request_background_removal_params_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


