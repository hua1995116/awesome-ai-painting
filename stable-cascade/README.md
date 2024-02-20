### stable-cascade 使用教程

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


## stable-cascade 介绍

是一个建立在Würstchen架构之上的创新文本到图像模型。Stable Cascade的显著特点在于其采用的三阶段方法，这种方法不仅在图像质量、灵活性和微调能力上达到了新的高度，而且极大地降低了对硬件的要求，使得在普通消费级硬件上进行训练和微调变得轻而易举。

https://github.com/Stability-AI/StableCascade
