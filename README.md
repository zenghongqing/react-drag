# 前端可视化拖拽平台

## 背景
（本项目为作者的毕业设计）

通过对可视化编辑系统的相关研究，以及对业务场景的思考，组件的抽象与拆分等。致力于解决当前前端开发人员较少，页面需求较多，重复需求多，复用性低的问 题。实现了一套基于 react 的前端可视化平台的系统。该平台可以为用户提供可视化编辑 前端页面并生成相应的 react 代码的功能。面向技术人员可用，打造一个通用的页面搭建平台。

## 系统设计

本系统的前端部分使用 React 技术作为视图框架。系统使用 umi 框架进行路由控制，使用 dva 进行状态管理。其中前 端依托 Node.js 作为中间层进行服务端的渲染，从而进一步提升页面首屏的渲染速度。 在前端的展示部分，通过 pages，layouts,以及 components 来配合完成。在状态管理部分， 配合 models，同时通过 dva 中的 connect 将视图与数据相连接。同时，对于前后端的请求， 通过 services 层实现。将一些常用的方法放置于 utils 下作为工具集。将有特殊含义的变量置于common。

## 总体功能
本系统的模块主要为用户管理、组织管理、页面拖拽编辑、页面预览导出以 及组件管理五大模块。其中由于使用 JWT 作为前后端登陆认证的方式，增加用户 认证模块。系统的核心功能流程是用户登陆系统，进入可视化页面编辑区，选择组件进行编辑，保存页面至服务器，构建相关代码，打包生成相应压缩包

## 运行平台

- 安装相关依赖 npm i
- 运行后台代码
- yarn start

## 效果展示
- 页面拖拽
![主页效果](http://q8bn25vr4.bkt.clouddn.com/01-%E6%8B%96%E6%8B%BD%E4%B8%BB%E9%A1%B5.png)
- 组件广场
![组件广场](http://q8bn25vr4.bkt.clouddn.com/02-%E7%BB%84%E4%BB%B6%E5%B9%BF%E5%9C%BA.png)
- 代码预览
![代码预览](http://q8bn25vr4.bkt.clouddn.com/03-%E4%BB%A3%E7%A0%81%E9%A2%84%E8%A7%88.png)
- 组织广场
![代码预览](http://q8bn25vr4.bkt.clouddn.com/04-%E7%BB%84%E7%BB%87%E5%B9%BF%E5%9C%BA.png)


## 功能
- 登陆
- 注册
- 页面（组件）编辑
    - 复制组件
    - 删除组件
    - 组件组合，生成组件模版
    - 修改属性
- 代码预览
- 组件广场
    - 分为个人组件，组织组件，以及公共组件，根据不同的权限展示不同的组件
    - 预览组件
    - 编辑组件
- 组织管理
    - 申请组织
    - 管理申请列表，同意或拒绝
