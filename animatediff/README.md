# Awesome AnimateDiff Guide

AnimateDiff usage in this repository is organized around three common workflows:

- CLI: https://github.com/s9roll7/animatediff-cli-prompt-travel
- ComfyUI: https://github.com/Kosinkadink/ComfyUI-AnimateDiff-Evolved
- WebUI: https://github.com/continue-revolution/sd-webui-animatediff

For most users, the learning curve is roughly WebUI, then ComfyUI, then CLI. The tools are different interfaces over similar core capabilities rather than direct replacements for one another.

## 0. Performance Boost

LCM AnimateDiff workflow for roughly 2x speed improvements:

[workflow_animatediff.json](./workflow_animatediff.json)

<img width="956" alt="AnimateDiff workflow screenshot" src="https://github.com/hua1995116/awesome-ai-painting/assets/12070073/77d235cf-63d8-4544-bcec-2b82f67221cc">

![AnimateDiff sample output](https://github.com/hua1995116/awesome-ai-painting/assets/12070073/54e84a30-9dd8-4bf7-885c-692a9034b256)

Twitter post: https://twitter.com/qiufenghyf/status/1723628793993322871

OpenPose example:

https://www.reddit.com/r/StableDiffusion/comments/17s7vl8/its_so_fast_lcm_lora_controlnet_openpose/

## 1. Tutorials

### CLI Tutorials

#### [Guide: Workflow for Creating Animations Using animatediff-cli-prompt-travel Step by Step](https://simpleaiart.com/sd-animatediff-cli-prompt-travel?a=b)

Summary:

Creates a sequence of still images and then stitches them together with AnimateDiff.

#### [AnimateDiff CLI Prompt Travel: IPAdapters, LoRAs, and Embeddings](https://www.youtube.com/watch?v=IxoXq9PiPis)

Summary:

This video explains how to use IP-Adapter, LoRA, and embeddings with the CLI prompt-travel workflow. It focuses on mixing text prompts with image prompts and shows how those controls affect the final animation.

Highlights:

- IP-Adapter can blend image guidance with text prompts.
- LoRAs can be layered into the workflow for style control.
- Embeddings are another practical lever for steering results.
- The tutorial includes concrete setup steps and output examples.

#### [A New AI Video Tool with Strong Potential: animatediff-cli-prompt-travel](https://www.bilibili.com/video/BV1w34y137Bu/?spm_id_from=333.337.search-card.all.click&vd_source=8d16a2bc27ef95a22c29f9a40f8f5633)

Summary:

Introduces AnimateDiff as a practical wrapper around AI video generation workflows, with ControlNet and IP-Adapter support for style transfer, script-to-video experiments, short-form social content, and comic-to-video work.

### ComfyUI Tutorials

#### [ComfyUI AnimateDiff Prompt Travel: Unlimited Animation Length](https://www.youtube.com/watch?v=L45Xqtk8J0I)

Summary:

A lightweight introduction to AnimateDiff in ComfyUI.

#### [ComfyUI Setup and AnimateDiff-Evolved Workflow with ControlNet OpenPose and QRCode Monster](https://www.youtube.com/watch?v=GV_syPyGSDY)

Summary:

A very long but detailed walkthrough of advanced AnimateDiff usage in ComfyUI.

#### [ComfyUI AnimateDiff Guide and Workflows Including Prompt Scheduling](https://civitai.com/articles/2379)

Summary:

- Includes `video2video` examples.
- Includes `text2video` examples.
- Includes multi-ControlNet `video2video` examples.

### SDXL Support

https://civitai.com/articles/2601

https://huggingface.co/hotshotco/Hotshot-XL/tree/main

https://github.com/hotshotco/Hotshot-XL

https://www.reddit.com/r/StableDiffusion/comments/1740eh8/now_we_can_try_hotshotxl_in_comfyui/

https://zhuanlan.zhihu.com/p/663187463

### WebUI Tutorials

#### [AnimateDiff Was Just Updated and Now Supports Motion Control](https://www.bilibili.com/video/BV1N34y1G7pm)

Summary:

Explains the latest plugin update and how to guide character motion with prompts.

Highlights:

- Noticeably smoother AI video output.
- Prompt-based control over subtle motion.
- Easy-to-use panel with a recommendation to use the latest `15_V2` release.
- Settings for both short GIFs and longer video runs.
- Straightforward installation with a good path for staying updated.

#### [Local AnimateDiff Installation for Very Long Animations](https://www.bilibili.com/video/BV1RF411C7ix)

Summary:

Shows how to install AnimateDiff locally, explains the approximate 12 GB VRAM requirement, and demonstrates how code changes can extend the default duration limit.

## 2. Model Collection

The core AnimateDiff release currently centers on three motion base models and eight motion LoRAs:

`mm_sd_v14.ckpt`

`mm_sd_v15.ckpt`

`mm_sd_v15_v2.ckpt`

`v2_lora_PanLeft.ckpt`

`v2_lora_PanRight.ckpt`

`v2_lora_RollingAnticlockwise.ckpt`

`v2_lora_RollingClockwise.ckpt`

`v2_lora_TiltDown.ckpt`

`v2_lora_TiltUp.ckpt`

`v2_lora_ZoomIn.ckpt`

`v2_lora_ZoomOut.ckpt`

Download:

https://huggingface.co/guoyww/animatediff/tree/main

## 3. Ecosystem

### CLI

https://github.com/s9roll7/animatediff-cli-prompt-travel

### WebUI

https://github.com/continue-revolution/sd-webui-animatediff

### ComfyUI

https://github.com/Kosinkadink/ComfyUI-AnimateDiff-Evolved

- https://github.com/FizzleDorf/ComfyUI_FizzNodes
- https://github.com/Kosinkadink/ComfyUI-Advanced-ControlNet
- https://github.com/Kosinkadink/ComfyUI-VideoHelperSuite
- https://github.com/Fannovel16/comfyui_controlnet_aux

## 4. Industry Examples

https://twitter.com/DiffusionPics/status/1716597134257164448

https://twitter.com/FinanceYF5/status/1709022312824226047

https://github.com/hua1995116/awesome-ai-painting/assets/12070073/ea4e60ca-0fa8-449b-9a33-549a1fb1b665

https://twitter.com/slimesunday/status/1709326883626615095

https://github.com/hua1995116/awesome-ai-painting/assets/12070073/c5582186-cd13-44c6-b3e8-8363280392bc

https://twitter.com/TDS_95514874/status/1708103034214219897

https://github.com/hua1995116/awesome-ai-painting/assets/12070073/200ecd03-4508-42ce-9762-ea9d5098639a

https://twitter.com/c0nsumption_/status/1711160317726597153

https://github.com/hua1995116/awesome-ai-painting/assets/12070073/f0a5b51a-450a-41f7-a684-8c9de80d56d9
