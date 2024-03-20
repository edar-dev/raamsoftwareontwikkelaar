---
title: Fine-Tuning Your Hugo Dev Environment
description: Dive into the essentials of setting up a development environment tailored for your Hugo project.
date: 2024-03-09T20:58:45.545Z
preview: ""
tags:
    - GitPod
    - Hugo
    - Dev Environment
categories: []
type: default
---

## Introduction

Embarking on my first Hugo project, I encountered my initial hurdle: configuring a proficient development environment.

Given Hugo's reputation for being lightweight and rapid, I opted for a **Cloud Development Environment**, ensuring accessibility from anywhere without the hassle of setup. My preferred choice? [GitPod](https://www.gitpod.io/). However, if you lean towards a traditional local environment, fear not; you can seamlessly follow this guide.

For insights into how I established my cloud development environment, check out my comprehensive guide [link].

## Install Hugo

The first step in crafting your Hugo development environment is installing Hugo itself. The official documentation offers an exhaustive [explanation](https://gohugo.io/installation/). However, my preferred method is:

``` sh
brew update 
brew install hugo hugo 
hugo version
```

For Windows environments, whether local or in the cloud, I recommend using Scoop. You can install Hugo with the following command:

``` powershell
scoop install hugo-extended
```

Once everything is installed correctly, execute 'hugo version' in your terminal, and you should see the version number printed out.

## Ide configuration and extensions

My IDE choice always goes to [Visual Studio Code](https://code.visualstudio.com/). If you follow me with the Cloud Development Environment path, you should have it already installed; otherwise, you can easily install it following the installation guide on the official site.

Let's tune our favorite IDE to make our lives way easier. My philosophy for this project is "less is more," meaning that I'm looking for the minimum set of extensions that make the job without losing any essential feature.

### FrontMatter 

A big part of the game for me is [Front Matter](https://marketplace.visualstudio.com/items?itemName=eliostruyf.vscode-front-matter). This extension is a fancy CMS integrated into our IDE. It allows us to create new content with the ease of a click, manage drafts and publications, start a local Hugo server, and much more. But with great power comes tricky configurations. Let's see how I configure mine:

The first time you install the extension, you can follow the tutorial to create the initial configuration. After that, a new file called frontmatter.json will be created in your solution. Here's how I edit it:

```json
"frontMatter.content.pageFolders": [
    {
      "title": "content",
      "path": "[[workspace]]/content",
      "filePrefix": ""
    },
    {
      "title": "hugo",
      "path": "[[workspace]]/content/note/hugo",
      "filePrefix": "",
      "previewPath": "/note/hugo"
    },
    {
      "title": "project",
      "path": "[[workspace]]/content/project"
    }
  ]

This configuration allows us to choose the folder in which we'd like to create new content, provide meaningful titles to remember our website structure, and override the default behavior of adding the current date as a prefix to the file name with the filePrefix property. Don't forget to update the previewPath property; otherwise, Front Matter assumes that the content is always at the root level while loading the preview.