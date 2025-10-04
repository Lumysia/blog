---
# --- Core Content ---
title: '数字小窝诞生记：缘起与初心'
subtitle: ""
date: '2025-10-04T02:16:49Z'
draft: false
description: "一直觉得 Homelab 听起来很复杂？其实超简单！这是我搭建“数字小窝”系列的第一篇文章，分享了我的入门硬件选择清单和从零开始的全部心路历程。快来看看如何拥有一个只属于你自己的服务器吧！"

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
  - 硬件
  # Type/Style
  - 入门

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

## 缘起

一听到“Homelab”（家庭实验室）这个词，是不是感觉有点吓人？好像是只有大神才会在秘密实验室里捣鼓的东西？其实完全不是啦！别担心，这比你想象的要简单得多！啊啊啊啊，求你了，千万别关掉这个页面，我发誓我没有在开玩笑！！！

虽然我是一个软件工程的学生，但我可以向你保证，这真的不是什么“专业工作”。它更像是在搭建一个数字版的乐高城堡。老实说，只要你能独立注册一个 GitHub 账号，你就已经掌握了开启这场冒险所需要的全部魔法咒语啦。

在这场冒险里，我的秘密武器就是 Docker 啦。别把它想成是什么可怕的技术，它更像一个超级贴心的小伙伴，能帮你把所有东西都整理得井井有条。之后我会专门为这个小可爱写一整篇文章的～

那么～我是怎么掉进“自托管”这个美妙的兔子洞的呢？这一切都始于我超棒的 gap year（其实是两年，哈哈），那段时光给了我一个完美的小角落，让我可以尽情地做梦和折腾。

那时候，我基本上天天都泡在各种科技产品的网店里，“云逛街”的同时幻想着该用哪些零件来组装我的完美小服务器。当然啦，我早就准备好了一份小小的愿望清单！

- 我需要一个《我的世界》服务器来和朋友们一起玩，所以需要一颗性能给力点的 CPU。
- 我想要运行一大堆服务，比如我自己的 Git 服务、用来存文件的 Nextcloud，还有看剧看电影的 Jellyfin。
- 我需要超大的空间来存放我的媒体文件和各种私藏宝贝，所以目标是至少 10TB。

我得承认，我这种把所有东西都塞进一个盒子里的“All-in-One”策略，并不能算是最佳实践，因为它没有把存储和计算分开。但是！我从中学到了超多东西，也收获了双倍的快乐，这难道不才是最重要的吗？我只要祈祷它哪天不要真的“一波炸”了就好，哈哈。

下一步是什么呢？当然是分享我的“装备清单”和它们的价格啦！

## 我的装备清单

> 这是我的小服务器的“配方”和价格（单位是加元 CAD）。如果你喜欢，可以把它当作灵感哦！～

| 类型 | 品牌 | 注释 | 价格 |
| - | - | - | - |
| NVME SSD | Lexar | 4T*2 | ~$270*2 = $540 |
| NVME SSD | Fanxiang | 2T | ~$140 |
| CPU | Intel | 13400 | ~$158 |
| Motherboard | Maxsun | Z790 | ~$260 |
| Memory | Glowy | 16G*2 | ~$120 |
| Memory | Kingbank | 16G*2 | ~$140 |
| Cooler | Thermalright | AXP90X53 | ~$30 |
| Power Supply | Seasonic | SUG300 | ~$100 |
| Computer Case | N/A | N/A | ~$40 |

> 一个给我自己（也给你们！）的小小便利贴：这块梵想的固态硬盘情绪有点……不稳定。我计划在 2027 年前把它换成一块更可靠的三星。你们可以从我踩过的小坑里学习经验哦～ (´-ω-)`

### 几个友好小提示

1. 在买任何亮闪闪的新玩具之前，一定先想好你到底想用它来做什么。
2. 主板和 CPU 是最好的朋友，它们必须合得来！通常最好是先选好 CPU，再去找一块喜欢它的主板。（当然，如果你对某块主板一见钟情，反过来也完全可以！）
3. DDR5 内存有时候会有点“小公主脾气”。我的小服务器就因为内存频率问题闹过好几次情绪，自己重置了 BIOS。所以尽量买主板厂商官方测试过、认证过的内存条。
4. 买一个好的、可靠的电源。这是服务器的心脏！既然它要 7x24 小时全年无休地工作，你肯定不想在这方面省钱的。
5. 你也可以用机械硬盘来获得超大空间，但我对它们“咔哒咔哒”的歌声超级敏感，所以……这个就得你自己选择啦。

接下来呢？今天就到这里啦！硬件是这个游戏的第一关。等你通关之后，下一道咒语就会在这本强大的魔法书里自动浮现哦～

## 最后再说几句

你心里是不是有小问号在冒泡呀？有什么地方觉得困惑吗？请务必，务必，务必在下面的讨论区里提出来！这里没有什么“傻问题”，我保证。只要我看到，就会立刻回复你。

把这么长的文章读到最后的你，希望你也有美好的一天！非常感谢你的耐心。如果你喜欢我的小故事，记得到我的“关于”页面里的讨论区来跟我打个招呼呀～
