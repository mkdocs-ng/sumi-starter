---
template: landing.html
title: My Project
description: One sentence that says what My Project does and who it is for.
hero:
  eyebrow: "Version 1.0 · open source"
  title: "Say what it does<br>*in five words.*"
  text: "Replace this with two sentences about the problem My Project solves and why someone should care. Keep it concrete: who uses it, and what gets easier."
  actions:
    - {text: Get started, link: guide/install.md, icon: rocket, primary: true}
    - {text: Read the guide, link: guide/index.md, icon: book-open}
  install: pip install my-project
  code:
    title: example.py
    lang: python
    content: |
      from my_project import Client

      client = Client()          # reads MY_PROJECT_TOKEN
      result = client.run("hello")
      print(result.summary)
sections:
  - type: features
    eyebrow: Why My Project
    title: Three or six reasons, each in one line.
    text: Replace these with what makes your project worth trying.
    items:
      - icon: zap
        title: Fast by default
        text: Say what is fast and give a number if you have one.
        link: guide/quick-start.md
      - icon: shield-check
        title: Safe to adopt
        text: Mention compatibility, licences, or how upgrades work.
        link: reference/configuration.md
      - icon: plug
        title: Fits your stack
        text: List the tools, languages or platforms it works with.
        link: guide/install.md
  - type: steps
    eyebrow: Three minutes
    title: From install to first result.
    items:
      - title: Install
        text: "`pip install my-project`"
      - title: Configure
        text: "Set `MY_PROJECT_TOKEN` or write a `my-project.toml`."
      - title: Run
        text: "`my-project run hello` prints a summary."
  - type: cta
    title: Ready to try it?
    text: The guide takes about ten minutes.
    actions:
      - {text: Start the guide, link: guide/index.md, primary: true}
      - {text: Star on GitHub, link: "https://github.com/example/my-project", icon: brand-github}
---

# My Project
