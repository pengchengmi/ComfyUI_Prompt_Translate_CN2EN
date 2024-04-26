# 百度爬虫 + 百度API翻译支持 阿里云有问题，暂停使用。
    已无需手动安装，在config.py 文件中，添加 阿里云/百度翻译 API的密钥+ key
    其他启动主程序，会自动安装所需要的文件。

    issue：
    linux 无法使用？
    在容器内 安装 node.js 环境解决。
    
 |  [English](#1-baidutranslateapi-install) | [中文教程](#comfyui-提示词翻译插件) | [视频教程](https://www.bilibili.com/video/BV1qw411Q7U9/?share_source=copy_web&vd_source=09df7e2da9d48d5fb9dcfe4ed69f071b) | [更新内容](#历史更新内容) |
# ComfyUI Prompt Translate to English
    introduction:
    1. I created two translation nodes, which can be both installed or only one of them can be used；
    2. first one is `BaiduTranslateApi`, it's used BaiduTranslate developer account 
       on the official website of Baidu Translator, which can be used for a long time by oneself;
    3. second is `BaiduTranslate`, Connected to the Api of Baidu Translate， Need install requirements；
    4. unable to preview the prompt words in Comfyui, i dont know how to do it. If you have any good ideas, Let me know!
    5. I didn't use Google Translate because I need to use it in China.
## 1. `BaiduTranslateApi` install
1. Download **Baidutranslate** zip，Place in `custom_nodes` folder, Unzip it；
2. Go to ‘[Baidu Translate Api](https://fanyi-api.baidu.com/?fr=pcHeader)’ and register a developer account，get your `appid` and `secretKey`；
3. Open the file `config.py` in Notepad/other editors;
4. Fill your `apiid` in quotation marks of `appid = ""` ；
4. Fill your `secretKey` in quotation marks of `secretKey = ""`；
6. Save file.

## 2. ‘AliyunApi’ install
1. go config.py;
2. fill apiid and key.

## 3. `PreviewText` Nodes
1. Preview translate result。

## 4. How to use
1. Nodes in Prompt translate list，if you use own Api, use `翻译Api auto to English`；
2. you can install both, whatever use.
![节点使用演示](./img/BaiduTranslate.png)
-----
# ComfyUI 提示词翻译插件
    简介：
    1. 有两个版本，一个是`BaiduTranslateApi`，这个需要去百度翻译官网注册开发者账号，可以自己长久使用。
    2. 第二个版本是`BaiduTranslate`，我爬了百度翻译的接口，不被百度反爬也可以长期使用。
    3. 暂时没法在comyfui中预览到提示词和修改，涉及到知识盲区，若大家有好的想法可以提出来！
## 1. `BaiduTranslateApi`的安装教程
1. 下载 **Baidutranslate** 压缩包，放到`custom_nodes`文件夹中；
2. 先去百度翻译，在上面点开 ‘[翻译API](https://fanyi-api.baidu.com/?fr=pcHeader)’ 注册一个开发者账号，获得你的`appid`和`secretKey`；
3. 记事本/其他编辑器打开文件`config.py`；
4. `appid = ""` **引号**之中填写你的百度翻译`apiid`；
5. `secretKey = ""`  **引号**之中填写你的百度翻译 `secretKey`；
6. 保存文件.

## 2. '阿里云'Api的安装教程
1. 和百度云一样。

## 3. `PreviewText` 节点
1. 预览翻译的结果；
2. 感谢B站网友给的建议，以及B站用户【阿米吉】提供的代码与思路。

## 4. 使用教程
1. 节点在Prompt translate列表中，如果用自己的Api，直接用`翻译Api auto to English`；
2. 也可以两个都安装，随便用一个，本质上没啥区别。
![节点使用演示](./img/BaiduTranslate.png)

# 历史更新内容
### 2023-9-01
1. 更新了文本预览节点

### 2023-09-14
1. 更新 可以在翻译节点内，选择翻译成语言，这样可以用作反推提示词。

### 2023-10-05
1. 更新了文本预览的实现方式，看看还有没有 冻结的问题。

### 2023-11-18
1. 大佬shiertier更新支持阿里云，并做优化。

### 2023-12-03
1. 修复阿里云不能部署的问题；
2. 优化阿里云导入失败，可以继续使用百度云的问题。
