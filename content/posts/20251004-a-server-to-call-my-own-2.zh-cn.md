---
# --- Core Content ---
title: '数字小窝诞生记：向世界敞开大门'
subtitle: ""
date: '2025-10-04T14:33:13-04:00'
draft: false
description: ""

# --- Author ---
author: "Lumysia"
authorLink: ""
license: ""

# --- Images ---
images: []
#featuredImage: ""
#featuredImagePreview: ""

# --- Taxonomies ---
categories:
  - 数字家园
tags:
  # Topic
  - Homelab
  - 网络
  - Cloudflare Tunnel
  - Python
  # Type/Style
  - 入门
  - 教程

# --- Page Behavior ---
hiddenFromHomePage: false
hiddenFromSearch: false

# --- Page Features ---
twemoji: false
lightgallery: true
ruby: true
fraction: true
fontawesome: true
linkToMarkdown: true
rssFullText: false

toc:
  enable: true
  auto: true

# --- Advanced Configuration ---
code:
  copy: true
  maxShownLines: 50
math:
  enable: false
mapbox:
share:
  enable: true
comment:
  enable: true
library:
  css:
    # someCSS = "some.css"
    # located in "assets/"
    # Or
    # someCSS = "https://cdn.example.com/some.css"
  js:
    # someJS = "some.js"
    # located in "assets/"
    # Or
    # someJS = "https://cdn.example.com/some.js"
seo:
  images: []
  # ...
---

> 本文由 Gemini 2.5 Pro 翻译

## 你的数字城堡的地基

那么，我们已经集齐了所有闪亮的硬件！现在，我们的小小数字家园应该建在哪里呢？是传统的、舒适的 Windows 小屋？还是极客范的、可定制的 Linux 树屋？又或者是花里胡哨又费钱的 macOS 别墅？

老实说，对于新手来说，这些选择中的任何一个都完全没问题，你完全可以用它们来开始你的家庭实验室冒险。这是你的世界，你来定规则！

但是！我今天想向你介绍的主角是神奇的 [Proxmox Virtual Environment](https://pve.proxmox.com/wiki/Main_Page)。哦哦哦，这听起来是不是超级技术宅？别担心！把它想象成一片神奇的土地。在这片土地上，你可以建造一栋 Windows 房子、一栋 Linux 房子，甚至一栋 macOS 房子，它们都可以作为快乐的小邻居和睦相处！对于我们想要构建的所有其他有趣的东西来说，它是一个完美、可靠的地基。

你可以跟着这篇[官方指南](https://pve.proxmox.com/wiki/Installation)来准备好你自己的那片 Proxmox 小天地。或者，如果你更喜欢，暂时继续使用你最爱的 Windows、Linux 或 macOS 也完全可以。你才是这场冒险的老大！

系统只是我们数字小窝所建立的土地，所以我们不会在这里花太多时间。如果你不确定如何安装操作系统，YouTube 上有大量非常有用的视频。我真的、真的、真的推荐你去看看！

## 让我们为你的数字家园敞开大门

好啦，你已经有了网络连接，你的网络服务提供商（ISP）也处理了所有无聊的事情。我们来做点超级刺激的事怎么样？想不想在大概 5 分钟内，搭建一个超简单的迷你网站并向全世界展示它吗？我们开始吧！

首先……你知道你的电脑是什么操作系统，对吧？嘿嘿，开个玩笑！

### Windows 10/11 的小伙伴们看这里

1. 用 Python 召唤一点小魔法
   1. 首先，同时按下键盘上的 `Win` 键和 `R` 键。在弹出的小框里，输入 `powershell` 然后按 `Enter`。这样就打开了我们的魔法命令窗口！
   2. 现在，让我们念出第一句咒语。复制下面这行并粘贴到 PowerShell 窗口里：`winget install Python.Python.3.13` 然后按 `Enter`。这是在告诉你的电脑为我们安装 Python！（一个小提示：这个版本在 2025 年 10 月算是非常新的，所以一些旧脚本可能会对它有点“小脾气”，但我个人总是喜欢最新最闪亮的东西！）
   3. **超级重要！** 关闭 PowerShell 窗口，然后重新打开一个全新的。这样能让我们的电脑知道我们刚刚安装的新魔法。
   4. 输入 `python -m http.server` 然后按 `Enter`。你应该会看到类似 `Serving HTTP on :: port 8000` 的消息。如果你看到了……嗒哒！
2. 访问你的杰作
   1. 看到消息里的那个 `8000` 了吗？那是你新服务器的秘密门牌号！我们去看看吧。打开任何网页浏览器，然后访问这个地址：`http://127.0.0.1:8000`。
   2. 你看到了什么？啊哈！是你的用户主文件夹，对吧？这是因为你念出 Python 咒语的地方就在那里。
3. 秘密通道：Cloudflare 隧道
   1. 让我们来安装我们的秘密武器！打开一个新的 PowerShell 窗口，输入这句咒语：`winget install Cloudflare.cloudflared`，然后按 `Enter`。
   2. 完成之后，就是最后的附魔了！在同一个窗口里，输入：`cloudflared tunnel --url http://127.0.0.1:8000`
   3. 给它大概 10 秒钟施展魔法……你有没有看到一大堆文字弹出来，还有一个特殊的 `trycloudflare.com` 链接？

    ```log
    2025-10-04T19:05:45Z INF Thank you for trying Cloudflare Tunnel. Doing so, without a Cloudflare account, is a quick way to experiment and try it out. However, be aware that these account-less Tunnels have no uptime guarantee, are subject to the Cloudflare Online Services Terms of Use (https://www.cloudflare.com/website-terms/), and Cloudflare reserves the right to investigate your use of Tunnels for violations of such terms. If you intend to use Tunnels in production you should use a pre-created named tunnel by following: https://developers.cloudflare.com/cloudflare-one/connections/connect-apps
    2025-10-04T19:05:45Z INF Requesting new quick Tunnel on trycloudflare.com...
    2025-10-04T19:05:48Z INF +--------------------------------------------------------------------------------------------+
    2025-10-04T19:05:48Z INF |  Your quick Tunnel has been created! Visit it at (it may take some time to be reachable):  |
    2025-10-04T19:05:48Z INF |  https://gem-saw-passed-equilibrium.trycloudflare.com                                      |
    2025-10-04T19:05:48Z INF +--------------------------------------------------------------------------------------------+
    2025-10-04T19:05:48Z INF Cannot determine default configuration path. No file [config.yml config.yaml] in [~/.cloudflared ~/.cloudflare-warp ~/cloudflare-warp]
    2025-10-04T19:05:48Z INF Version 2025.8.1 (Checksum b5d598b00cc3a28cabc5812d9f762819334614bae452db4e7f23eefe7b081556)
    2025-10-04T19:05:48Z INF GOOS: windows, GOVersion: go1.24.2, GoArch: amd64
    2025-10-04T19:05:48Z INF Settings: map[ha-connections:1 protocol:quic url:http://127.0.0.1:8000]
    2025-10-04T19:05:48Z INF cloudflared will not automatically update on Windows systems.
    2025-10-04T19:05:48Z INF Generated Connector ID: 3f5d9474-b25a-44f0-987a-2140fbf9a9c1
    2025-10-04T19:05:48Z INF Initial protocol quic
    2025-10-04T19:05:48Z INF ICMP proxy will use 192.168.1.233 as source for IPv4
    2025-10-04T19:05:48Z INF ICMP proxy will use fdaa:2937:24e1::80e in zone Wi-Fi as source for IPv6
    2025-10-04T19:05:48Z ERR Cannot determine default origin certificate path. No file cert.pem in [~/.cloudflared ~/.cloudflare-warp ~/cloudflare-warp]. You need to specify the origin certificate path by specifying the origincert option in the configuration file, or set TUNNEL_ORIGIN_CERT environment variable originCertPath=
    2025-10-04T19:05:48Z INF cloudflared does not support loading the system root certificate pool on Windows. Please use --origin-ca-pool <PATH> to specify the path to the certificate pool
    2025-10-04T19:05:48Z INF ICMP proxy will use 192.168.1.233 as source for IPv4
    2025-10-04T19:05:48Z INF Tunnel connection curve preferences: [X25519MLKEM768 CurveP256] connIndex=0 event=0 ip=198.41.200.73
    2025-10-04T19:05:48Z INF ICMP proxy will use fdaa:2937:24e1::80e in zone Wi-Fi as source for IPv6
    2025-10-04T19:05:48Z INF Starting metrics server on 127.0.0.1:20241/metrics
    2025-10-04T19:05:48Z INF Registered tunnel connection connIndex=0 connection=ea01956f-739a-4251-aeb4-ea9b96f24037 event=0 ip=198.41.200.73 location=yyz06 protocol=quic
    ```

4. 向世界问好！去吧，复制那个链接，在你的浏览器里打开它！屏幕上是什么？没错！是你那个小小的 Python 网页服务器！你没有关掉它，对吧？哈哈。现在，世界上任何拥有那个秘密链接的人都能看到它了。你成功啦！

### macOS 的朋友们看这里

1. 召唤 Python
   1. 打开你的 `终端`。（按 `Cmd + Space`，输入 `终端`，然后按 `Enter`）。
   2. 念出这句咒语：`python3 -m http.server`
   3. 嗒哒！就这么简单！你的小服务器应该已经在运行了。你现在可以在浏览器里访问 `http://127.0.0.1:8000` 来看它。
2. 获取你的魔法大锅：Homebrew
   1. 你的 Mac 有一个超酷的魔法大锅叫做 Homebrew，它几乎能帮你搞定任何你需要的工具！首先，我们打开 `终端`。按 `Cmd + Space` 打开聚焦搜索，输入 `终端`，然后按 `Enter`。
   2. 输入 `brew --version` 来检查你是否已经安装了 Homebrew。如果你看到了版本号，就可以跳到下一步了！如果没有，就复制下面这整句咒语并粘贴到终端里来安装它：`/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`
   3. 它可能会问你要密码。别担心，这是安全的！
3. 开启隧道！
   1. 输入 `brew install cloudflared` 然后按 `Enter`。
   2. 最后的魔法戏法，输入：`cloudflared tunnel --url http://127.0.0.1:8000`
   3. 几秒钟后，你就会得到一个专属于你的特别 `trycloudflare.com` 链接。把它分享给朋友，向他们展示你的魔法吧！

### Linux 的探险家们看这里

对于所有的 Linux 奇才们，我感觉你们可能已经知道这个小技巧了！步骤和 Windows 的非常相似，我完全相信你们！你们能搞定的！

### 但是……刚才那通魔法到底是怎么回事？

所以我们费这么大劲是为了什么？我为什么要为你设计这个小魔术呢？秘密就在这里。

把你家的路由器想象成一个非常严格但用心良苦的城堡守卫。它的工作就是保护你家里所有的设备（你的电脑、你的手机）免受互联网上可怕事物的侵害。它会给你所有的设备一个秘密的、内部的 IP 地址，只有城堡里的人才能看到。

问题是，这个守卫太尽职尽责了，以至于当一个来自外部世界的友好访客，试图用你的公共 IP 地址来访问你新建的 Python 网站时，守卫只会说“不行！”然后“砰”地一声关上大门。这是每个人都会遇到的一个非常普遍的问题！

那么，Cloudflare 隧道是怎么工作的呢？它的魔法是什么？

嗯，Cloudflare 隧道就像一个神秘的皇家信使！它不是从外面试图砸开城堡的大门，而是从你的城堡内部（你的电脑）开始，创建一条通往外界的安全、秘密的隧道。任何拥有秘密地址（就是那个 trycloudflare.com 链接）的人都可以给信使一条消息，然后信使会安全地把它带回你城堡内部的服务器。

那个坏脾气的城堡守卫甚至都不用打开主城门！是不是很聪明？(´-ω-)`

## 充满魔力的总结

看看你！你刚刚用一句 Python 咒语凭空召唤出了一个小小的 Web 服务器，然后用 Cloudflare 隧道为全世界打开了一扇可以窥探它的魔法传送门！你应该为自己感到超级骄傲！

现在，这个“快速隧道”是个非常有趣的派对小把戏，对吧？这就像在我们的数字家门口向全世界大喊“你好！”，也是让我们初尝成功的完美方式！但如果你想创建一个私密的、舒适的空间，只让你自己的设备之间相互交谈，而不让全世界都来偷看呢？

这正是我们下一趟冒险的内容！我们将要学习一种叫做 Tailscale 的全新魔法。与向公众敞开大门不同，Tailscale 帮助我们只为自己的设备建立一个秘密的魔法网络。这就像创建一个私人的小俱乐部，你的笔记本电脑、手机和新服务器都可以在里面互通秘密，无论它们身处世界的哪个角落！通过它自己独特的咒语 `tailscale serve`，我们将会看到在我们专属的俱乐部里共享服务是多么的容易。

感谢你今天成为如此出色的魔法学徒！我们下次再见！(´-ω-)`
