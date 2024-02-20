# 脚本说明

- 该脚本是一个用于学习参考的示例，主要用于jd账号密码自动登录，最后抓取网页中的数据并提交到青龙中。然而，请注意该脚本目前存在一些bug。
- 第一次使用脚本后会自动生成一个配置文件`jdck.config`，你可以修改该配置文件来设置登录账号、密码等信息，以及青龙对接容器等。
- 此外，我们也提供了一个可供下载的exe程序，可以直接运行，无需配置环境。

## 注意事项

- 第一次使用脚本时会有`[INFO] Starting Chromium download.`进度条加载，请耐心等待。这是用于加载浏览器，如果加载速度太慢或失败导致程序报错退出，请尝试更换网络，或者多试几次。
- 暂时不开发autman插件，因为一个月要5块钱，如果有兴趣开发的插件的朋友请踊跃尝试，代码都有明确的注释，但请免费开源！请免费开源！请免费开源！
- 目前还比较适合于windows平台。

## 功能特点

- 通过模拟滑块操作来绕过京东的滑块验证。
- 提供了一些基本的自动化操作示例。
- 根据设置的账号密码自动登录jd账号，并抓取某个网页的值提交到青龙中。

## 使用方法

1. 安装必要的依赖：
   ```python
   import asyncio  # 异步I/O操作库
   import random  #用于模拟延迟输入
   from re import T  # 随机数生成库
   import cv2  # OpenCV库，用于图像处理
   from pyppeteer import launch  # pyppeteer库，用于自动化控制浏览器
   import aiohttp   #用于请求青龙
   from urllib import request  # 用于网络请求，这里主要用来下载图片
   from PIL import Image  #用于图像处理
   import os  #读取配置文件
   ```

## 配置登录信息：
打开生成的配置文件jdck.config，根据需要修改其中的账号、密码等登录以及青龙对接容器等。
   ```python
Displaylogin=1  #是否显示登录操作，1显示，0不显示
qlip=http://192.168.1.1:5700
client_id=*******
client_secret=*******

上面是配置参数，下面保存账户密码

备注1#登录账号1#登录密码
备注2#登录账号2#登录密码
备注3#登录账号3#登录密码
账号格式以此类推
   ```

## 运行脚本：
运行脚本或者双击运行下载的exe程序即可自动模拟操作京东滑块验证。脚本会自动加载浏览器并完成滑块验证。

免责声明
本脚本仅供学习参考，请勿用于非法用途。
作者不对因使用该脚本造成的任何损失或法律问题负责。
