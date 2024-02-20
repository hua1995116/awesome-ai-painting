## stable-cascade 使用教程

[English](./README_en.md) [中文](./README.md)

1.安装最新版本的 Comyfui

2.将 https://huggingface.co/stabilityai/stable-cascade/tree/main 下面的 stage_b 和 stage_c 模型放到 ComfyUI/models/unet 下面

3.将 https://huggingface.co/stabilityai/stable-cascade/tree/main 下面的 stage_a 模型

4.将 clip 模型 https://huggingface.co/stabilityai/stable-cascade/tree/main/text_encoder 放到 ComfyUI/models/clip

说明：

stage_b 和 stage_c 可以根据显存选择不同的组合，组合如下（以下组合越往下显存消耗越小）: 

- stage_b.safetensors + stage_c.safetensors
- stage_b_bf16.safetensors + stage_c_bf16.safetensors
- stage_b_lite.safetensors + stage_c_lite.safetensors
- stage_b_lite_bf16.safetensors + stage_c_lite_bf16.safetensors

Comyfui 工作流

[stable_cascade_workflow_test.json](https://github.com/hua1995116/awesome-ai-painting/files/14339725/stable_cascade_workflow_test.json)


## stable-cascade 训练教程

目前 kohya_ss 已经支持了早期的 stable-cascade 训练

https://github.com/bmaltais/kohya_ss/tree/stable-cascade

训练示例：

https://github.com/bmaltais/kohya_ss/tree/stable-cascade/examples/stable_cascade

训练启动示例(官方中有部分参数异常训练会报错)

```
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

## stable-cascade 介绍

是一个建立在Würstchen架构之上的创新文本到图像模型。Stable Cascade的显著特点在于其采用的三阶段方法，这种方法不仅在图像质量、灵活性和微调能力上达到了新的高度，而且极大地降低了对硬件的要求，使得在普通消费级硬件上进行训练和微调变得轻而易举。

https://github.com/Stability-AI/StableCascade
