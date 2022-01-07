---
title: yarn常用命令
date: 2022-01-07 17:40:28
tags:
---

yarn安装

npm i yarn -g

查看版本

Yarn -v
<!-- more -->
## 1、开始一个新工程

yarn init 与 npm init 一样通过交互式会话创建一个 package.json

yarn init # yarn

跳过会话，直接通过默认值生成 package.json

yarn init --yes # 简写 -y

## 2、添加一个依赖

通过 yarn add 添加依赖会更新 package.json 以及 yarn.lock 文件

1).开发环境

yarn add  packageName  依赖会记录在 package.json 的 dependencies 下 开发环境

yarn add webpack@2.3.3 # yarn --save 是 yarn 默认的，默认记录在 package.json 中

2).生产环境

yarn add  packageName  --dev 依赖会记录在 package.json 的 devDependencies 下生产环境

yarn add webpack --dev # yarn 简写 -D

3).全局

yarn global add  packageName  全局安装依赖

yarn global add webpack # yarn

## 3、更新一个依赖

yarn upgrade 用于更新包到基于规范范围的最新版本

## 4、移除一个依赖

yarn remove

## 5、安装 package.json 中的所有文件

yarn 或者 yarn install

## 6、运行脚本

yarn run 用来执行在 package.json 中 scripts 属性下定义的脚本

// package.json
{
  "scripts": {
      "dev": "node app.js",
      "start": "node app.js"
  }
}

yarn run dev # yarn 执行 dev 对应的脚本 node app.js

## 7、显示某个包信息

yarn info <packageName> 可以用来查看某个模块的最新版本信息

## 8、列出项目的所有依赖

yarn list # 列出当前项目的依赖

