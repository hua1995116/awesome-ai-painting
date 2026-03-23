## Stable Cascade Guide

### Setup

1. Install the latest version of ComfyUI.
2. Place the `stage_b` and `stage_c` model files from https://huggingface.co/stabilityai/stable-cascade/tree/main into `ComfyUI/models/unet`.
3. Place the `stage_a` model files from the same repository in the location required by your ComfyUI setup.
4. Place the CLIP text encoder from https://huggingface.co/stabilityai/stable-cascade/tree/main/text_encoder into `ComfyUI/models/clip`.

Notes:

`stage_b` and `stage_c` can be mixed and matched depending on your available VRAM. The combinations below are ordered from highest to lowest VRAM usage:

- `stage_b.safetensors` + `stage_c.safetensors`
- `stage_b_bf16.safetensors` + `stage_c_bf16.safetensors`
- `stage_b_lite.safetensors` + `stage_c_lite.safetensors`
- `stage_b_lite_bf16.safetensors` + `stage_c_lite_bf16.safetensors`

### ComfyUI Workflow

[stable_cascade_workflow_test.json](https://github.com/hua1995116/awesome-ai-painting/files/14339725/stable_cascade_workflow_test.json)

## Training

`kohya_ss` already supports early Stable Cascade training:

https://github.com/bmaltais/kohya_ss/tree/stable-cascade

Training example:

https://github.com/bmaltais/kohya_ss/tree/stable-cascade/examples/stable_cascade

Launch example:

The original upstream example contains a few parameters that can fail in practice. This version is the adjusted command used in this repository:

```bash
accelerate launch --mixed_precision bf16 --num_cpu_threads_per_process 8 stable_cascade_train_stage_c.py \
  --mixed_precision bf16 --save_precision bf16 --max_data_loader_n_workers 2 --persistent_data_loader_workers \
  --gradient_checkpointing --learning_rate 1e-4 \
  --optimizer_type adafactor --optimizer_args "scale_parameter=False" "relative_step=False" "warmup_init=False" \
  --max_train_epochs 10 --save_every_n_epochs 1 --save_precision bf16 \
  --output_dir "/root/autodl-tmp/kohya_ss/output" --output_name "testv1" \
  --stage_c_checkpoint_path "/root/autodl-tmp/ckpts/stage_c_bf16.safetensors" \
  --effnet_checkpoint_path "/root/autodl-tmp/ckpts/effnet_encoder.safetensors" \
  --previewer_checkpoint_path "/root/autodl-tmp/ckpts/previewer.safetensors" \
  --dataset_config "/root/autodl-tmp/kohya_ss/examples/stable_cascade/test_dataset.toml" \
  --sample_every_n_epochs 1 --sample_prompts "/root/autodl-tmp/kohya_ss/examples/stable_cascade/prompt.txt" \
  --adaptive_loss_weight
```

## Overview

Stable Cascade is a text-to-image model built on the Wurstchen architecture. Its three-stage design improves image quality, flexibility, and fine-tuning potential while also lowering hardware requirements enough to make consumer-grade training and adaptation much more practical.

https://github.com/Stability-AI/StableCascade
