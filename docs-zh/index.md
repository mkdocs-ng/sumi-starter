---
template: landing.html
title: 我的项目
description: 用一句话说明这个项目做什么、给谁用。
hero:
  eyebrow: "1.0 版 · 开源"
  title: "用一句话<br>*说清它做什么。*"
  text: "把这里换成两句话：项目解决什么问题、为什么值得一试。尽量具体，说清谁在用、什么变简单了。"
  actions:
    - {text: 开始使用, link: guide/install.md, icon: rocket, primary: true}
    - {text: 阅读指南, link: guide/index.md, icon: book-open}
  install: pip install my-project
  code:
    title: example.py
    lang: python
    content: |
      from my_project import Client

      client = Client()          # 读取环境变量
      result = client.run("hello")
      print(result.summary)
sections:
  - type: features
    eyebrow: 为什么选它
    title: 三到六个理由，每个一句话。
    text: 把这些换成你的项目真正的亮点。
    items:
      - icon: zap
        title: 默认就快
        text: 说明哪里快，有数字就写数字。
        link: guide/quick-start.md
      - icon: shield-check
        title: 放心采用
        text: 写兼容性、许可证或升级方式。
        link: guide/install.md
      - icon: plug
        title: 融入现有工具
        text: 列出它支持的工具、语言或平台。
        link: guide/install.md
  - type: cta
    title: 准备好试试了吗？
    text: 读完指南大约需要十分钟。
    actions:
      - {text: 开始阅读, link: guide/index.md, primary: true}
      - {text: 在 GitHub 上关注, link: "https://github.com/example/my-project", icon: brand-github}
---

# 我的项目
