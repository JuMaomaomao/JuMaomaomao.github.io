---
title: pnpm
date: 2022-01-11 15:39:45
tags:
---

## 什么是pnpm——个人不完全解读
pnpm同npm和yarn一样，是一个包管理工具。pnpm的出现是为了解决node_modules占用过大的问题。当我们的电脑上存储了多个项目时，node_modules的占用就会很大，而使用pnpm，所有的依赖会被存储在内容可寻址的存储中，即存储在硬盘的同一位置，当我们需要安装的依赖在硬盘中已经存在，包里的文件会硬链接到这一位置而不是重新安装，这样多个项目可以共享同一依赖
<!-- more -->
## pnpm常用命令
## 管理依赖
安装依赖
`pnpm add sax`------------保存到 dependencies
`pnpm add -D sax`---------保存到 devDependencies
`pnpm add -O sax`---------保存到 optionalDependencies
`pnpm add sax@next`-------安装 next tag
`pnpm add sax@3.0.0`------安装指定版本 3.0.0

安装项目所有依赖
`pnpm install`

根据指定的范围更新软件包的最新版本
`pnpm update`

从 node_modules 和项目的 package.json 中移除包
`pnpm remove`

使当前本地包可在系统范围内或其他位置访问
`pnpm link <dir>`
`pnpm link --global`
`pnpm link --global <pkg>`

取消链接一个系统范围的package (相对于 pnpm link)
`yarn unlink`

从另一个软件包管理器的 lock 文件生成 pnpm-lock.yaml
`pnpm import`

重建一个package
`pnpm rebuild`

移除不需要的软件包
`pnpm prune`

## 查看依赖
检查已安装包的已知安全问题
`pnpm audit`

以一个树形结构输出所有的已安装package的版本及其依赖
`pnpm list`

检查过期的 packages
`pnpm outdated`

## 运行脚本
运行一个在 package的 manifest 文件中定义的脚本
`pnpm run`

运行在 package 的 scripts 对象中test 属性指定的任意的命令。
`pnpm test`