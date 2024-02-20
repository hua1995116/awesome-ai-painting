## Tutorial for using stable-cascade

[English](./README_en.md) [中文](./README.md)

1. Install the latest version of Comyfui

2. Place the stage_b and stage_c models from https://huggingface.co/stabilityai/stable-cascade/tree/main under ComfyUI/models/unet

3. Place the stage_a model from https://huggingface.co/stabilityai/stable-cascade/tree/main

4. Place the clip model from https://huggingface.co/stabilityai/stable-cascade/tree/main/text_encoder into ComfyUI/models/clip

Explanation:

Stage_b and stage_c can be combined differently depending on the VRAM available. The combinations below are listed from the most to the least VRAM consumption:

- stage_b.safetensors + stage_c.safetensors
- stage_b_bf16.safetensors + stage_c_bf16.safetensors
- stage_b_lite.safetensors + stage_c_lite.safetensors
- stage_b_lite_bf16.safetensors + stage_c_lite_bf16.safetensors

### Comyfui Workflow

[stable_cascade_workflow_test.json](https://github.com/hua1995116/awesome-ai-painting/files/14339725/stable_cascade_workflow_test.json)


## Training tutorial for stable-cascade

Kohya_ss now supports early training of stable-cascade

https://github.com/bmaltais/kohya_ss/tree/stable-cascade

Training example:

https://github.com/bmaltais/kohya_ss/tree/stable-cascade/examples/stable_cascade


## Introduction to stable-cascade

Stable Cascade is an innovative text-to-image model built upon the Würstchen architecture. Its notable feature is the three-stage approach, which not only achieves new heights in image quality, flexibility, and fine-tuning capabilities but also significantly lowers hardware requirements. This makes training and fine-tuning on standard consumer-grade hardware straightforward and accessible.

https://github.com/Stability-AI/StableCascade
