# ImageGenerationRequestTextToImageParams

Parameters for TEXT_IMAGE task

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**text** | **str** | Text prompt | [optional] 
**negative_text** | **str** | What NOT to include | [optional] 
**style** | **str** |  | [optional] 
**condition_image** | **bytearray** | Base64-encoded conditioning image | [optional] 
**control_mode** | **str** |  | [optional] [default to 'CANNY_EDGE']
**control_strength** | **float** |  | [optional] [default to 0.7]

## Example

```python
from quantcdn.models.image_generation_request_text_to_image_params import ImageGenerationRequestTextToImageParams

# TODO update the JSON string below
json = "{}"
# create an instance of ImageGenerationRequestTextToImageParams from a JSON string
image_generation_request_text_to_image_params_instance = ImageGenerationRequestTextToImageParams.from_json(json)
# print the JSON string representation of the object
print(ImageGenerationRequestTextToImageParams.to_json())

# convert the object into a dict
image_generation_request_text_to_image_params_dict = image_generation_request_text_to_image_params_instance.to_dict()
# create an instance of ImageGenerationRequestTextToImageParams from a dict
image_generation_request_text_to_image_params_from_dict = ImageGenerationRequestTextToImageParams.from_dict(image_generation_request_text_to_image_params_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


