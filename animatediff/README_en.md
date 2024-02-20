# Awesome AnimateDiff Tutorial

[English](./README_en.md) [中文](./README.md)

Recently, I studied [AnimateDiff](https://github.com/guoyww/AnimateDiff) and summarized its usage for users. From the information I organized, the high-level applications can be divided into three categories:

- cli (https://github.com/s9roll7/animatediff-cli-prompt-travel)
- comfyui (https://github.com/Kosinkadink/ComfyUI-AnimateDiff-Evolved)
- webui (https://github.com/continue-revolution/sd-webui-animatediff)
 
The ease of getting started with these tools is ranked as webui > comfyui > cli. There is no replacement among them; my understanding is that the difference lies in the human-computer interaction interface, but all methods can achieve consistent effects. However, the webui plugin currently still has some model gray pictures, but in terms of ecology, webui is more powerful.

# 0. Performance Boost

LCM AnimateDiff Workflow Scheme (Speed up by 100%):

[workflow_animatediff.json](./workflow_animatediff.json)

<img width="956" alt="WeChat20f30d01961352caad9b01adda2fbafe" src="https://github.com/hua1995116/awesome-ai-painting/assets/12070073/77d235cf-63d8-4544-bcec-2b82f67221cc">

![AnimateDiff_00165_](https://github.com/hua1995116/awesome-ai-painting/assets/12070073/54e84a30-9dd8-4bf7-885c-692a9034b256)

Twitter address: https://twitter.com/qiufenghyf/status/1723628793993322871

Openpost example:

https://www.reddit.com/r/StableDiffusion/comments/17s7vl8/its_so_fast_lcm_lora_controlnet_openpose/

# 1. Tutorials

## CLI Tutorials

### [Guide: Workflow for Creating Animations using animatediff-cli-prompt-travel Step-by-Step](https://simpleaiart.com/sd-animatediff-cli-prompt-travel?a=b)

*Summary*

Mainly uses AWPainting to produce a series of images, then strings them together with Animatediff for teaching.

### [AnimateDiff CLI prompt travel: IPAdapters, LoRAs, and Embeddings](https://www.youtube.com/watch?v=IxoXq9PiPis)

*Summary (GPT Summary)*
This video introduces how to use AnimateDiff CLI prompt travel, focusing mainly on Lora embeddings and IP adapter. Lora can be mixed with text prompts, while the IP adapter allows the use of image prompts. The video author used both IP adapter and Lora for easier handling. Besides, the video also mentions embedding, a method to influence the result. Finally, the video demonstrates how to set up IP adapter and Lora and showcases the generated result.

*Highlights*
🎬 Introduction of Lora embeddings and IP adapter
🌟 IP adapter can be mixed with text prompts, Lora allows the use of image prompts
📚 Embedding is a method to influence the result
🖥️ Steps to set up IP adapter and Lora
🚀 Showcase of generated results

### [New AI Video Creation Tool with Huge Potential! What Opportunities Exist in the Video Sector with animatediff-cli-prompt-travel?](https://www.bilibili.com/video/BV1w34y137Bu/?spm_id_from=333.337.search-card.all.click&vd_source=8d16a2bc27ef95a22c29f9a40f8f5633)

*Summary (GPT Summary)*

This video introduces a new tool, AnimateDiff, which is a wrapper based on AnimateDiff to solve some pain points in AI video creation and introduces ControlNet and IP Adapter. Its features include style conversion, controlling image details in videos, quick script-to-video conversion, TikTok-style videos, comic-to-video conversion, etc., showcasing its huge potential.

*Highlights*

- 🎨 AnimateDiff is a new AI video creation tool that can address some challenges
- 🎞️ It enables style conversion and control over image details in videos
- 🚀 Suitable for quick script-to-video conversions, TikTok-style videos, comic-to-video conversions, etc.
- 🤖 Incorporates ControlNet and IP Adapter, showing huge potential
- 📈 Offers significant opportunities for creative video production with a large market potential

## ComfyUI Tutorials

### [ComfyUI AnimateDiff Prompt Travel: Unlimited Animation Length!](https://www.youtube.com/watch?v=L45Xqtk8J0I)

*Summary*

Introduces entry-level operations using animatediff comfyui, simple and fast

### [ComfyUI Setup & AnimateDiff-Evolved Workflow + ControlNet OpenPose and QRcode Monster](https://www.youtube.com/watch?v=GV_syPyGSDY)

*Summary*

Details on various operations using animatediff comfyui, lasting 5 hours, very long but very detailed

### [ComfyUI AnimateDiff Guide/Workflows Including Prompt Scheduling - An Inner-Reflections Guide](https://civitai.com/articles/2379)

*Summary*

- Includes video2video examples
- Includes text2video examples
- Includes video2video with multiple controlnet controls examples

### SDXL Support

https://civitai.com/articles/2601

https://huggingface.co/hotshotco/Hotshot-XL/tree/main

https://github.com/hotshotco/Hotshot-XL

https://www.reddit.com/r/StableDiffusion/comments/1740eh8/now_we_can_try_hotshotxl_in_comfyui/

https://zhuanlan.zhihu.com/p/663187463

## WebUI Tutorials

### [Animatediff got updated yesterday! Now you can control the actions, hurry up and make an animated little sister!](https://www.bilibili.com/video/BV1N34y1G7pm)

*Summary (GPT Summary)*

The video introduces the update of the animatediff plugin and how to use the plugin to control the actions of a little sister.

*Highlights*

- 🤩 Significant improvement in AI video creation quality, smooth and fluid
- 🤔 Control subtle movements of a little sister through descriptive words
- 🚀 Simple and user-friendly panel, recommend the latest version 15_V2
- 💡 Optimized settings allow for the creation of a complete animated GIF or a stable long video
- 💻 Easy installation, recommended to install yourself for real-time updates

### [Animation Freedom? Generating Unlimited Long Animations, Local Installation of AnimateDiff](https://www.bilibili.com/video/BV1RF411C7ix)

*Summary (GPT Summary)*
Sharing today is about the AI open-source software AnimateDiff, which can generate long animations and requires 12GB of VRAM. By changing the code, you can break the three-second length limit and generate longer animations.

*Highlights*
- 🎞️ AnimateDiff can generate long animations, requires 12GB of VRAM, optimized to run on a 3090 graphics card.
