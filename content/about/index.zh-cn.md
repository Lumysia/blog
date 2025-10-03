---
# --- Core Content ---
title: '关于'
description: "A brief page description for SEO and previews."
date: '2025-10-03T19:42:26Z'
lastmod: '2025-10-03T19:42:26Z'
draft: false

# --- Taxonomies ---
tags:
categories:

# --- Author ---
authors:
  - Lumysia

# --- Featured Image ---
image:
  src: "" # Path to the image (e.g., /images/posts/hello.jpg)
  alt: "" # Alt text for SEO and accessibility
  caption: "" # Optional caption below the image

# --- Page Behavior ---
build:
  render: true # Set to `never` to prevent this page from being built
  list: true # Set to `never` to hide from lists (homepage, archives, etc.)
  publishResources: true

# --- Page Features ---
features:
  toc: true
  comment: true
  share: true
  math: false

# --- Advanced Configuration ---
code:
  copy: true
  maxShownLines: 50
seo:
  # Override the default social media image (which uses `image.src`)
  images: [] # e.g., ["/images/posts/hello-social.jpg"]
assets:
  # Load page-specific CSS or JS files (relative to the `assets` directory)
  css: []
  js: []
---

## 关于我

嗨，我是Livia！欢迎来到《璐㛓娅的魔法书》—— 我在互联网上的温馨小天地。

我最近搬到了加拿大奥沙瓦，在安大略理工大学攻读软件工程硕士学位。

这个博客是我的个人空间，用来分享我的故事与思考，内容包括：

- 我的生活点滴。
- 未来在维护家庭服务器与开发软件方面的探索。
- 日常的所思所想及其他有趣的故事。

欢迎来到我新的精神家园。

## 联系方式

- 电子邮件: <sovranova@outlook.com>
  - PGP Key: [CEAD651C8780CF74](/gpg-lumysia-pubkey.asc)

## 朋友们

<style>
  .friends-grid {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 1.5rem;
    list-style-type: none;
    padding: 0;
    margin-top: 2rem;
  }

  .friend-card {
    border: 1px solid var(--border-color, #eee);
    background: var(--card-background, #fafafa);
    border-radius: 8px;
    padding: 1rem;
    transition: transform 0.2s, box-shadow 0.2s;
    text-align: left;
  }
  .friend-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 4px 12px rgba(0,0,0,0.1);
  }

  .card-header {
    display: flex;
    align-items: center;
    margin-bottom: 0.75rem;
  }

  .card-avatar {
    width: 45px;
    height: 45px;
    border-radius: 50%;
    object-fit: cover;
    margin-right: 10px;
  }

  .card-name {
    font-weight: bold;
    font-size: 1.1em;
    color: var(--body-color);
  }

  .card-description {
    font-size: 0.85em;
    color: var(--secondary-color, #777);
    margin: 0;
  }

  .friend-card a {
    text-decoration: none;
    color: inherit;
  }

  body[theme="dark"] .friend-card {
    border: 1px solid #333;
    background: #252627;
  }
  body[theme="dark"] .friend-card:hover {
    box-shadow: 0 4px 12px rgba(0,0,0,0.3);
  }

  @media (max-width: 768px) {
    .friends-grid {
      grid-template-columns: 1fr 1fr;
    }
  }
  @media (max-width: 480px) {
    .friends-grid {
      grid-template-columns: 1fr;
    }
  }
</style>

<div class="friends-grid">

  <div class="friend-card">
    <a href="https://meiza.cc/" target="_blank" rel="noopener noreferrer">
      <div class="card-header">
        <img src="https://meiza.cc/wp-content/uploads/2024/11/%E9%80%8F%E6%98%8E%E5%BA%95812264566f14da8ea7f525b8cb97fc1e-01.png" alt="Meiza的头像" class="card-avatar">
        <span class="card-name">Meiza</span>
      </div>
      <p class="card-description">
        你找到啦~ 欢迎来到Meiza的小盒 – 这里是meiza的个人网站！
      </p>
    </a>
  </div>

  <div class="friend-card">
    <a href="https://example.com" target="_blank" rel="noopener noreferrer">
      <div class="card-header">
        <img src="https://i.pravatar.cc/300" alt="示例头像" class="card-avatar">
        <span class="card-name">示例朋友</span>
      </div>
      <p class="card-description">
        示例描述.
      </p>
    </a>
  </div>
  
  <div class="friend-card">
    <a href="https://example.com" target="_blank" rel="noopener noreferrer">
      <div class="card-header">
        <img src="https://i.pravatar.cc/300" alt="示例头像" class="card-avatar">
        <span class="card-name">示例朋友</span>
      </div>
      <p class="card-description">
        示例描述.
      </p>
    </a>
  </div>

</div>
