# ImageGenerationRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**model_id** | **str** | Model to use for image generation | [optional] [default to 'amazon.nova-canvas-v1:0']
**task_type** | **str** | Type of image generation task | 
**text_to_image_params** | [**ImageGenerationRequestTextToImageParams**](ImageGenerationRequestTextToImageParams.md) |  | [optional] 
**color_guided_generation_params** | [**ImageGenerationRequestColorGuidedGenerationParams**](ImageGenerationRequestColorGuidedGenerationParams.md) |  | [optional] 
**image_variation_params** | [**ImageGenerationRequestImageVariationParams**](ImageGenerationRequestImageVariationParams.md) |  | [optional] 
**in_painting_params** | [**ImageGenerationRequestInPaintingParams**](ImageGenerationRequestInPaintingParams.md) |  | [optional] 
**out_painting_params** | [**ImageGenerationRequestOutPaintingParams**](ImageGenerationRequestOutPaintingParams.md) |  | [optional] 
**background_removal_params** | [**ImageGenerationRequestBackgroundRemovalParams**](ImageGenerationRequestBackgroundRemovalParams.md) |  | [optional] 
**virtual_try_on_params** | **object** | Parameters for VIRTUAL_TRY_ON task | [optional] 
**image_generation_config** | [**ImageGenerationRequestImageGenerationConfig**](ImageGenerationRequestImageGenerationConfig.md) |  | [optional] 
**region** | **str** | AWS region for Nova Canvas | [optional] [default to 'us-east-1']

## Example

```python
from quantcdn.models.image_generation_request import ImageGenerationRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ImageGenerationRequest from a JSON string
image_generation_request_instance = ImageGenerationRequest.from_json(json)
# print the JSON string representation of the object
print(ImageGenerationRequest.to_json())

# convert the object into a dict
image_generation_request_dict = image_generation_request_instance.to_dict()
# create an instance of ImageGenerationRequest from a dict
image_generation_request_from_dict = ImageGenerationRequest.from_dict(image_generation_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


