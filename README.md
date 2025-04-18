
# :dress: Fashion AI

### Overview

#### This Colab notebook demonstrates how AI can transform the clothes in your photos based on simple text descriptions.  


![Fashion_AI_Examples](https://github.com/user-attachments/assets/2ca84aa2-7157-416c-bb29-c443646c6f6f)



Just upload a picture, click to auto-generate mask for the area of the photo you need to transform, tell the AI what outfit you'd like to see, and watch it work its magic !  

https://github.com/user-attachments/assets/3e017cff-94de-4b86-9b82-b83ef94e0f70

### Google colab notebook link:
https://colab.research.google.com/github/Patcharinee/Fashion_AI/blob/main/Fashion_AI_1_5.ipynb


### Approach
Fashion AI consists of the following key components:

- SAM (Segment Anything Model) by Meta AI for automatic mask generation based on user clicks. **(**https://segment-anything.com/**)**
- Stable Diffusion for AI-powered outfit generation from text descriptions.
- ControlNet with Canny Edges to modify selected clothing areas while preserving the rest of the image based on the Canny edges of the original image. (https://huggingface.co/lllyasviel/sd-controlnet-canny)
- Diffusers Stable Diffusion ControlNet Inpaint Pipeline for Inpainting; the process of replacing or editing specific areas of an image i.e., masked area. Note that Inpainting relies on a mask to determine which regions of an image to fill in; the area to inpaint is represented by white pixels and the area to keep is represented by black pixels. The white pixels are filled in by the user text prompt. (https://huggingface.co/docs/diffusers/v0.33.1/using-diffusers/inpaint)
- Gradio for creating a user interface for user image uploading, mask area selection, mask editing, text prompt input, outfit generation, and result display. (https://www.gradio.app/)
