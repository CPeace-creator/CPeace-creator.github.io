---
title: UniPush 推送项目
date: 2025-03-16 16:39:00
keywords: 项目
cover: https://raw.githubusercontent.com/CPeace-creator/picGo/main/raffle-pic.jpg
sticky: 0
toc: true
categories:
- 项目
reward: true
---

# UniPush 推送项目

本项目基于 **uni-app** 开发，实现了 **实时推送、抽奖大转盘、订单同步等功能**，并结合 **uniCloud 云开发** 进行服务端处理，支持 **H5 端和微信小程序** 的无缝部署。

## 核心功能

### 抽奖系统

- **大转盘 UI 设计**：采用 **HTML + CSS** 还原炫酷的转盘抽奖界面，结合 **CSS animation** 动画提升用户体验。
- **抽奖逻辑**：基于 **uniCloud 云数据库** 存储抽奖规则，确保公平公正。

### 实时订单同步

- **多人点餐同步**：利用 **uni-push** 进行 **多人实时同步菜单**，无论在哪个端操作，都能快速更新数据。
- **扫码核销功能**：通过 **微信 API 生成小程序码**，用户扫码即可完成 **中奖核销**。

### 优化与扩展

- **分页加载**：借助 **z-paging 组件** 实现 **触底加载和下拉刷新**，提升数据加载流畅度。
- **防抖优化**：利用 `lodash.debounce` 避免高频网络请求，降低服务器压力。
- **定时任务**：基于 **云对象 timing 触发器** 定时执行任务，如 **定期开奖、清理无效订单**。

---

## 项目展示

> 以下截图做了适当裁剪，方便在博客内阅读。

### 抽奖活动页

<img src="https://raw.githubusercontent.com/CPeace-creator/picGo/main/20250308180107.png" width="60%">

- 采用 **大转盘动画**，增强交互体验。
- 抽奖结果由 **云函数** 计算，确保数据安全。

### 创建抽奖

<img src="https://raw.githubusercontent.com/CPeace-creator/picGo/main/20250308180505.png" width="60%">

- 管理员可自定义 **抽奖规则**、**奖品信息**，并设置开奖时间。
- **存储至 uniCloud 数据库**，支持实时更新。

### 记录获取

<img src="https://raw.githubusercontent.com/CPeace-creator/picGo/main/20250308180555.png" width="60%">

- **分页加载优化**，确保流畅浏览历史记录。
- 结合 **uniCloud** 实现 **数据筛选和排序**。

### 开启抽奖

<img src="https://raw.githubusercontent.com/CPeace-creator/picGo/main/20250308180620.png" width="60%">

- 倒计时结束后，自动触发 **uniCloud 云函数** 进行开奖。
- 中奖信息会 **实时推送至用户端**。

### 中奖核销

<img src="https://raw.githubusercontent.com/CPeace-creator/picGo/main/20250308180646.png" width="60%">

- 采用 **小程序码扫码核销**，保证领取的唯一性。
- 订单状态会 **实时更新至数据库**。

### 正在抽奖

<img src="https://raw.githubusercontent.com/CPeace-creator/picGo/main/20250308180709.png" width="60%">

- **动态 UI 展示**，提升抽奖仪式感。
- 结合 **CSS 动画**，让转盘更生动。

### 中奖状态

#### 未中奖

<img src="https://raw.githubusercontent.com/CPeace-creator/picGo/main/20250308180739.png" width="50%">

- 提示 **未中奖**，并提供 **参与更多抽奖活动** 的入口。

#### 已中奖

<img src="https://raw.githubusercontent.com/CPeace-creator/picGo/main/20250308180739.png" width="50%">

- 中奖用户可直接进入 **兑奖流程**，扫码核销后完成订单。

---

## 项目的功能点

1. 熟练应用 HTML + CSS 完成抽奖大转盘页面布局。
2. 使用 uni-app 组件及扩展组件完成多端交互开发。
3. 通过 z-paging 插件实现触底加载和下拉刷新。
4. 使用 CSS animation 实现更有表现力的动态效果。
5. 结合插件市场与 npm 管理项目依赖。
6. 掌握 uniCloud 云函数、JQL、schema 表与触发器。
7. 基于 uni-id 定制微信一键登录和账号登录。
8. 开启 uni-push 实时推送能力。
9. 通过 push 实现多人同步点餐菜单案例。
10. 使用 `lodash.debounce` 防抖优化网络开销。
11. 调用微信 API 生成并解析小程序码。
12. 实现扫码核销业务逻辑。
13. 使用云对象 timing 定时触发器处理任务。
14. 打包上线微信小程序和 H5 云端 Web 托管。

## 项目部分展示图

<img src="https://raw.githubusercontent.com/CPeace-creator/picGo/main/raffle-pic.jpg">

## 总结

本项目不仅实现了 **抽奖、实时推送、云开发** 的核心能力，还结合 **防抖、分页加载、定时任务** 等优化策略，确保系统具备较好的流畅度和可扩展性。同时依赖 **uni-app** 实现 **H5 与微信小程序** 的多端互通。
