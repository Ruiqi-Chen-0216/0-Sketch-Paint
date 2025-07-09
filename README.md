# 0-Sketch-Color
STAT402 Final Project Coding

This README file provides an overview of the coding part for our STAT402 Final Project. 

## Step 1: 0-Sketch

The codes for this step are primarily found in three notebooks: customized_stable_diffusion_pipeline.ipynb, kohya_LoRA_trainer.ipynb, and stable_diffusion_with_LoRAfile_added_ipynb.ipynb.

customized_stable_diffusion_pipeline.ipynb: This notebook is used to run and check for any bugs. If any bugs are found, they might be due to incorrect versions of the pipeline or Xformers. In this notebook, we utilized the "Anything_v_3" diffuser model. However, you can customize it by changing the model_id. Please ensure that the model_id exists and can be accessed via a URL. To generate colored images, modify the prompts and provide your own descriptions. Finally, execute the last generation process if all environments are properly set up and the pipelines are well-constructed.

stable_diffusion_with_LoRAfile_added_ipynb.ipynb: This notebook is similar to customized_stable_diffusion_pipeline.ipynb, with the addition of a function for loading LoRA weight files into UNet's attention layers. We extract weights from .safetensor files and merge them with the supported weights of the diffuser. Instead of converting the .safetensor into another format, we directly update the weight of the base model. Please note that this notebook does not support LoRA weight files containing weights for other modules like text encoder. Therefore, the example of animeoutlineV4.16.safetensors provided does not work here.

kohya_LoRA_trainer.ipynb: This notebook serves as a detailed LoRA weights trainer and can be run on Colab with GPU support. It is already customized and wrapped, requiring you to replace the parameters with your own preferences and prepare your training set. You can train the LoRA weights according to your needs. Please be aware that there might be a torch.size bug during the final training process due to changes in the versions of imported libraries used by this notebook's dependencies.

## Step 2: Sketch-Paint

For better user experience, we implement a simple GUI.
+ Dependencies are listed at the top of the file.
+ Feel free to run everything above and jump directly to the GUI part, and have fun with AI drawing 😸
