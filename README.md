# PaliGemma Fine-Tuning for VQA Tasks

This repository contains a Jupyter notebook (`PaliGemma-Finetuning.ipynb`) for fine-tuning the PaliGemma model on Visual Question Answering (VQA) tasks. The provided notebook resolves several common issues found in the official fine-tuning notebooks for PaliGemma, making it a valuable resource for users looking to fine-tune this model with minimal setup.

## Features

- **Error-Free Fine-Tuning:** This notebook addresses errors frequently encountered in official PaliGemma fine-tuning notebooks, ensuring a smoother experience for fine-tuning on VQA tasks.
- **Customizable for Any VQA Dataset:** The notebook is designed to work with datasets in the VQAv2 format, but can be adapted for other VQA datasets by adjusting columns accordingly.
- **Quantization Support:** The model is optimized with 4-bit quantization to reduce memory usage and computational cost.
- **LoRA Integration:** Low-Rank Adaptation (LoRA) is used to efficiently fine-tune the model with fewer parameters, helping improve the overall training process.
- **Preprocessing and Data Handling:** The notebook includes custom data collators and preprocessing functions to handle images and text inputs appropriately for the model.

## Requirements

The notebook requires the following Python packages:
- `peft` for LoRA integration
- `datasets` for loading the dataset
- `transformers` for handling the PaliGemma model
- `pillow` for image processing
- `bitsandbytes` for quantization support

The installations for these are included in the notebook and need not be performed separately

## Usage
The notebook is desgned for seamless use. Change the dataset cell to your desired dataset from the Hub, or in case you want to use your personal dataset, you can use the load_dataset() function from the datasets module in order to easily fit the dataset into the framework. If the dataset's format matches VQAv2, no further column name changes etc are required, otherwise modify the fields as needed. Once this is done, modify the hyperparameters as needed and finetune the model for your purposes. I hope this notebook proves useful for your work.
