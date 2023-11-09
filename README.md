
# 📷 Image Denoising with MMagic's DeNoise Model 🌟

This Python script demonstrates how to use the MMagic API to remove noise from images and enhance their quality using the DeNoise model. Simply provide an input image, and the script will generate a denoised output! 🧹🖼️

## Prerequisites 🛠️

Before you get started, make sure you have the following dependencies installed:

- Python 3.8 (or a compatible version) 🐍
- Miniconda ⚙️

## Installation Steps 📦

Follow these simple steps to set up your environment for using the MMagic DeNoise model:

1. **Install [Miniconda](https://docs.conda.io/projects/miniconda/en/latest/miniconda-install.html) on your system if you haven't already.**

2. **Create a Conda environment and activate it using the following commands:**

   ```bash
   conda create --name mmagic python=3.8 -y
   conda activate mmagic
   ```

3. **Check your CUDA version by running the command:**

   ```bash
   nvcc --version
   ```

4. **Download the model configuration and checkpoint from [Models-and-config.txt](Models-and-config.txt).**

5. **Get input and output image paths from the user.**

   ```bash
   Enter the input image path: input_image.png
   Enter the output image path: output_image.png
   ```

6. **Start the timer for performance measurement.**

7. **Create the MMagicInferencer using the provided model configuration and checkpoint.**

   ```python
   editor = MMagicInferencer('esrgan', model_config=config, model_ckpt=checkpoint)
   ```

8. **Remove noise from the input image and save the denoised output.**

   ```python
   output = editor.infer(img=input_img_path, result_out_dir=output_img_path)
   ```

9. **Stop the timer and print the inference time.**

   ```python
   end_time = time.time()
   print(f"Inference time: {end_time - start_time:.2f} seconds")
   ```

Now you're ready to enhance the quality of your images by removing noise with MMagic's DeNoise model! 📷✨

Make sure to provide the correct paths for your input and output images to enjoy beautifully denoised results. 🧼🌈
