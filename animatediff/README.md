# Awesome  AnimateDiff Tutorial

最近研究了一下 [AnimateDiff](https://github.com/guoyww/AnimateDiff), 对此用户进行了总结，从我整理的资料上来看，大体上使用的高阶应用分为三个种类：

- cli  (https://github.com/s9roll7/animatediff-cli-prompt-travel)
- comfyui (https://github.com/Kosinkadink/ComfyUI-AnimateDiff-Evolved)
- webui (https://github.com/continue-revolution/sd-webui-animatediff)
 
以上工具的容易上手程度 webui > comfyui > cli ， 他们之前不存在谁能代替谁，我的理解只是使用的人机交互界面不同，所有方式都能实现一致的效果。不过目前看起来 webui 插件目前还带有部分模型灰图的情况，但是生态来说 webui 更加强大。


# 0.性能提速

LCM AnimateDiff 工作流方案（提速100%）：

[workflow_animatediff.json](./workflow_animatediff.json)

<img width="956" alt="WeChat20f30d01961352caad9b01adda2fbafe" src="https://github.com/hua1995116/awesome-ai-painting/assets/12070073/77d235cf-63d8-4544-bcec-2b82f67221cc">

![AnimateDiff_00165_](https://github.com/hua1995116/awesome-ai-painting/assets/12070073/54e84a30-9dd8-4bf7-885c-692a9034b256)


twitter地址：https://twitter.com/qiufenghyf/status/1723628793993322871

openpost示例：

https://www.reddit.com/r/StableDiffusion/comments/17s7vl8/its_so_fast_lcm_lora_controlnet_openpose/


# 1.教程

## cli 教程

### [Guide: Workflow for Creating Animations using animatediff-cli-prompt-travel Step-by-Step](https://simpleaiart.com/sd-animatediff-cli-prompt-travel?a=b)

*摘要*

主要使用了用AWPainting制作一系列图片，然后通过 Animatediff 进行串联的教学

### [AnimateDiff CLI prompt travel: IPAdapters, LoRAs, and Embeddings](https://www.youtube.com/watch?v=IxoXq9PiPis)


*摘要(gpt总结)*
本视频介绍了如何使用AnimateDiff CLI prompt travel，主要关注Lora embeddings和IP adapter。Lora能够与文本提示进行混合，而IP adapter则允许使用图像提示。视频作者使用了IP adapter和Lora，以便更容易上手。除此之外，视频还提到了embedding，这是一种影响结果的方法。最后，视频演示了如何设置IP adapter和Lora，并展示了生成结果。

*亮点*
🎬 Lora embeddings和IP adapter的介绍
🌟 IP adapter能够与文本提示混合，Lora则允许使用图像提示
📚 Embedding是影响结果的方法
🖥️ IP adapter和Lora的设置步骤
🚀 展示了生成结果

### [AI视频生成新工具！animatediff-cli-prompt-travel拥有巨大潜力！视频赛道有哪些机会？](https://www.bilibili.com/video/BV1w34y137Bu/?spm_id_from=333.337.search-card.all.click&vd_source=8d16a2bc27ef95a22c29f9a40f8f5633)


*摘要(gpt总结)*

这个视频是介绍一个新工具AnimateDiff，它是基于AnimateDiff的一个封装，用来解决AI视频生成中的一些痛点，并引入了ControlNet和IP Adapter。它的特点是可以进行风格转换，控制视频中的图像细节，可以用来做快速脚本转视频，抖音风格视频，漫画转视频等，具有巨大的潜力。

*亮点*

- 🎨 AnimateDiff是一个AI视频生成的新工具，可以解决一些痛点
- 🎞️ 它可以进行风格转换，控制视频中的图像细节
- 🚀 可以用来做快速脚本转视频、抖音风格视频、漫画转视频等
- 🤖 引入了ControlNet和IP Adapter，拥有巨大的潜力
- 📈 可以用来做更多有意思的视频生成，具有非常大的市场机会




## comfyui教程

### [ComfyUI AnimateDiff Prompt Travel: Unlimited Animation Length!](https://www.youtube.com/watch?v=L45Xqtk8J0I)

*摘要*

介绍了使用 animatediff comfyui 的入门级别操作，简单快速

### [ComfyUI Setup & AnimateDiff-Evolved Workflow + ControlNet OpenPose and QRcode Monster](https://www.youtube.com/watch?v=GV_syPyGSDY)

*摘要*

详细介绍了使用 animatediff comfyui 的各种操作， 时长 5 个小时，非常久，但是非常详细


### [ComfyUI AnimateDiff Guide/Workflows Including Prompt Scheduling - An Inner-Reflections Guide](https://civitai.com/articles/2379)

*摘要*

- 包含video2video 示例
- 包含text2video 示例
- 包含video2video 多 controlnet 控制示例

### SDXL Suppport

https://civitai.com/articles/2601

https://huggingface.co/hotshotco/Hotshot-XL/tree/main

https://github.com/hotshotco/Hotshot-XL

https://www.reddit.com/r/StableDiffusion/comments/1740eh8/now_we_can_try_hotshotxl_in_comfyui/

https://zhuanlan.zhihu.com/p/663187463


## webui教程


### [animatediff昨天更新啦！ 可以控制动作了，赶紧做动起来的小姐姐吧！](https://www.bilibili.com/video/BV1N34y1G7pm)

*摘要(gpt总结)*

视频介绍了animatediff插件的更新情况，以及如何使用该插件来控制小姐姐的动作。

*亮点*

- 🤩 AI视频生成质量大幅提升，丝滑流畅
- 🤔 通过描述词来控制小姐姐的细微动作
- 🚀 简单易用的面板，推荐最新版本15_V2
- 💡 优化设置可以选择生成一段完整的动图或稳定的长串视频
- 💻 安装简单，建议自行安装以实时更新


### [动画自由？无限长动画生成，AnimateDiff本地化安装](https://www.bilibili.com/video/BV1RF411C7ix)

*摘要(gpt总结)*
今天要分享的是AI开源软件AnimateDiff，可以生成长动画，需要12G显存。通过改变代码可以突破三秒长度限制，生成更长的动画。

*亮点*
- 🎞️ AnimateDiff可以生成长动画，需要12G显存，优化后可在3090显卡上运行。
- 🚀 安装过程简单，按照文档安装即可。
- 🎨 通过改变代码可以突破三秒长度限制，生成更长的动画。
- 🎬 生成的动画可用于作为素材，配合剪辑会有更好的效果。
- 🤖 AnimateDiff提供了训练方法，可以让镜头更加丰富，动作更多，没有水印。 



# 2.模型合集

目前主要分为 3个运动主模型 和 8个 运动 lora

mm_sd_v14.ckpt

mm_sd_v15.ckpt

mm_sd_v15_v2.ckpt

v2_lora_PanLeft.ckpt

v2_lora_PanRight.ckpt

v2_lora_RollingAnticlockwise.ckpt

v2_lora_RollingClockwise.ckpt

v2_lora_TiltDown.ckpt

v2_lora_TiltUp.ckpt

v2_lora_ZoomIn.ckpt

v2_lora_ZoomOut.ckpt

下载地址：https://huggingface.co/guoyww/animatediff/tree/main

# 3.生态套件

## cli

https://github.com/s9roll7/animatediff-cli-prompt-travel


## webui

https://github.com/continue-revolution/sd-webui-animatediff

## comfyui

https://github.com/Kosinkadink/ComfyUI-AnimateDiff-Evolved

- https://github.com/FizzleDorf/ComfyUI_FizzNodes

- https://github.com/Kosinkadink/ComfyUI-Advanced-ControlNet

- https://github.com/Kosinkadink/ComfyUI-VideoHelperSuite

- https://github.com/Fannovel16/comfyui_controlnet_aux

# 4.业内 case

https://twitter.com/DiffusionPics/status/1716597134257164448


https://twitter.com/FinanceYF5/status/1709022312824226047


https://github.com/hua1995116/awesome-ai-painting/assets/12070073/ea4e60ca-0fa8-449b-9a33-549a1fb1b665


https://twitter.com/slimesunday/status/1709326883626615095

https://github.com/hua1995116/awesome-ai-painting/assets/12070073/c5582186-cd13-44c6-b3e8-8363280392bc


https://twitter.com/TDS_95514874/status/1708103034214219897


https://github.com/hua1995116/awesome-ai-painting/assets/12070073/200ecd03-4508-42ce-9762-ea9d5098639a



https://twitter.com/c0nsumption_/status/1711160317726597153



https://github.com/hua1995116/awesome-ai-painting/assets/12070073/f0a5b51a-450a-41f7-a684-8c9de80d56d9



https://twitter.com/DiffusionPics/status/1708937572880126338


https://github.com/hua1995116/awesome-ai-painting/assets/12070073/3633a181-6153-4788-877c-11c3b7306e11




https://www.youtube.com/watch?v=7_hh3wOD81s

https://www.reddit.com/r/StableDiffusion/comments/16xx177/ipadapters_in_animatediffcliprompttravel_another/?utm_source=share&utm_medium=web2x&context=3

https://www.reddit.com/r/StableDiffusion/comments/173rrc2/underwater_caustics_study_using_animatediff/

https://www.reddit.com/r/StableDiffusion/comments/1736k87/eleven_vs_one_details_in_comments/

https://www.reddit.com/r/StableDiffusion/comments/1734ns0/a1111_webui_animatediff_v19_updated_support/

https://www.reddit.com/r/StableDiffusion/comments/172lcxm/ai_revolution/

https://huggingface.co/viddle/viddle-pix2pix-animatediff

https://github.com/viddle-app/viddle-pix2pix-animatediff
