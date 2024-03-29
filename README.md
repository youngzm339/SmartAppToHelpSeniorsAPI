# SmartAppToHelpSeniorsAPI
[![License](https://img.shields.io/github/license/youngzm339/SmartAppToHelpSeniorsAPI)](https://github.com/youngzm339/SmartAppToHelpSeniorsAPI/blob/master/LICENSE)
[![Issues](https://img.shields.io/github/issues/youngzm339/SmartAppToHelpSeniorsAPI)](https://github.com/youngzm339/SmartAppToHelpSeniorsAPI/issues)
[![Stars](https://img.shields.io/github/stars/youngzm339/SmartAppToHelpSeniorsAPI)](https://github.com/youngzm339/SmartAppToHelpSeniorsAPI)

![SmartAppToHelpSeniorsAPI](https://azurecomcdn.azureedge.net/cvt-342af4abf51292fe470c0f54c8b878f696465f7b08177b0a21f80ffab347bd93/images/page/home/december-hero-desktop.webp)

README of supported languages: [English](./README.md)  |  [简体中文](./README-zh_CN.md)

## AI implementations based on Azure AI platform
This project does a number of AI implementations based on Azure AI platform. Before using it, please make sure you have introduced the KEY and other parameters correctly, check the code for the parameters you may need.

You may need to read [Azure Cognitive Services documentation](https://learn.microsoft.com/en-us/azure/cognitive-services/) to get a general idea of the features before using this project.

## Principles for Developers 
This is part of an project for participate in the 2023 Microsoft Imagine Cup.

By using this project, you should ensure that you follow the MIT license and DO NOT use this project to participate in the 2023 Microsoft Imagine Cup.

# ###
# ###
## Interface 
baseURL: example.com

# #########
### Speech to Text 
#### Request Address :
https://example.com/api/speech/speech2text

#### Request Method :
HTTP POST with multipart/form-data Content-Type

|key|vaule|
|---|---|
|audio_input|[audiofile](.mp3 or .wav)|

#### Example of request :
audio_input:[123.wav]

#### Example of response :
```
{
    "code": "200",
    "msg": "成功",
    "data": "这是语音生成的内容。"
}
```

# #########
### Text to Speech 
#### Request Address :
https://example.com/api/speech/text2speech
#### Request Method :
HTTP POST with multipart/form-data Content-Type

|key|vaule|
|---|---|
|text_input|"str"|

#### Example of request :
text_input:"语音生成"

#### Example of response :
[5123123213.wav]


# #########
### Customized Q&A
#### Request Address :
https://example.com/api/speech/talk

#### Request Method :
HTTP POST with multipart/form-data Content-Type

|key|vaule|
|---|---|
|text_input|"str"|

#### Example of request :
text_input:"支付宝怎么打开健康码"

#### Example of response :

```
{
    "code": "200",
    "msg": "成功",
    "input": "怎么打开健康码",
    "data": "首先打开【支付宝】客户端，然后在上方搜索栏搜索“健康码”，点击上方的【出示健康码】按钮，接着点击下方的【立即查看】按钮，申领电子健康卡后，点击上方的【电子健康卡】位置，进入【居民电子健康码】页面，再点击右上角的【…】图标，在弹出的选项栏点击【添加到桌面】选项，最后点击【立即添加】按钮即可。"
}
```

# #########
### Customized Q&A Audio
#### Request Address :
https://example.com/api/speech/talk_audio

#### Request Method :
HTTP POST with multipart/form-data Content-Type

|key|vaule|
|---|---|
|text_input|"str"|

#### Example of request :
text_input:"支付宝怎么打开健康码"

#### Example of response :
[5123123213.wav]


# #########
### Image Analysis 
#### Request Address :
https://example.com/api/cv/image4analysis

#### Request Method :
HTTP POST with multipart/form-data Content-Type

|key|vaule|
|---|---|
|img_input|Image file|

#### Example of response :

```
{
    "code": "200",
    "msg": "成功",
    "caption": "a sign on a pole",
    "caption-cn": "杆子上的标志",
    "tags": [
        "text",
        "outdoor",
        "sky",
        "sign",
        "street"
    ]
}
```
