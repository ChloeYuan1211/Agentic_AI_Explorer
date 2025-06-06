# Coze 使用指南

> **Coze** 是字节跳动推出的面向企业和开发者的 AI 聊天机器人与智能应用开发平台，支持多模型接入，拥有可视化工作流、低代码/零代码开发等能力，可广泛应用于客户服务、智能问答、业务流程自动化等场景。

---

## 目录

1. [平台简介](#平台简介)
2. [主要功能](#主要功能)
3. [注册与登录](#注册与登录)
4. [基础设置](#基础设置)
5. [创建与管理 Bot](#创建与管理-bot)
6. [知识库管理](#知识库管理)
7. [工作流与插件](#工作流与插件)
8. [团队协作](#团队协作)
9. [API 集成](#api-集成)
10. [常见问题与支持](#常见问题与支持)

---

## 平台简介

Coze 平台致力于为企业和开发者提供一站式 AI 机器人和智能应用解决方案。用户可以通过可视化界面快速搭建对话机器人、知识问答助手、业务自动化工具，并可无缝集成主流大模型如 GPT-4、Qwen、Claude、豆包等。

![Coze 产品架构图](https://docs.coze.com/imgs/coze_architecture.png)

---

## 主要功能

- **Bot 快速搭建**：无需代码即可创建和发布多场景智能机器人
- **多模型集成**：支持多种主流大模型接入和切换
- **知识库管理**：支持文档上传、结构化知识录入
- **工作流自动化**：可视化拖拽式流程设计，插件丰富
- **多渠道部署**：支持接入微信、钉钉、飞书、网页、小程序等
- **API/SDK 集成**：方便系统集成与扩展
- **团队管理与协作**：多成员权限管理

---

## 注册与登录

1. 访问 [Coze 官网](https://www.coze.com/)。
2. 点击“注册”或“立即体验”，使用邮箱或手机号注册账号。
3. 根据提示完善个人信息，完成注册后登录平台。

---

## 基础设置

### 1. 个人及团队信息

- 点击右上角头像，进入“个人中心”可修改昵称、绑定邮箱等。
- 支持创建和管理团队，设置成员权限和分组。

### 2. 选择/接入大模型

- 进入“模型管理”或“AI 服务”设置页面。
- 选择所需大模型并配置 API Key（如 GPT-4、Qwen、Claude、豆包等）。
- 可设置默认模型和备用模型。

---

## 创建与管理 Bot

### 1. 创建新 Bot

- 在“Bot 管理”页面点击“新建 Bot”。
- 填写 Bot 名称、描述，选择使用的 AI 模型。
- 选择 Bot 类型：问答机器人、客服助理、流程自动化等。

### 2. 配置 Bot 能力

- 配置 Bot 的欢迎语、默认回复、上下文管理等。
- 绑定知识库、接入插件、设置意图识别与多轮对话。
- 可视化拖拽设计对话流程与业务流程。

### 3. 测试与发布

- 在右侧测试区与 Bot 进行交互，调试效果。
- 点击“发布”即可部署到指定渠道（如微信、网页等）。

---

## 知识库管理

### 1. 创建知识库

- 进入“知识库”模块，点击“新建知识库”。
- 设置知识库名称、类型（FAQ、文档等）。

### 2. 文档上传与管理

- 支持上传 PDF、Word、Excel、TXT、网页等多种格式文档。
- 支持批量导入和自动解析。
- 可手动补充和编辑知识点。

### 3. 智能问答配置

- 设置知识库的召回方式和问答准确度。
- 支持人工标注和多轮问答训练。

---

## 工作流与插件

- 进入“工作流”或“插件市场”，选择需要的自动化流程或插件。
- 可视化拖拽设置触发条件、处理步骤和输出内容。
- 支持第三方系统集成，如表单、数据库、OA 系统等。
- 插件可扩展 Bot 能力，实现如天气查询、表单收集、自动推送等功能。

---

## 团队协作

- 可邀请团队成员，设置为管理员、成员、访客等不同角色。
- 支持 Bot 和知识库的协同开发与共享。
- 管理成员权限，保证数据与流程安全。

---

## API 集成

1. 在“开发者中心”获取 API Key 和文档。
2. 按照文档调用 Coze 的 RESTful API，实现与外部系统的数据交互和集成。

```bash
curl -X POST https://api.coze.com/v1/bot/{bot_id}/invoke \
     -H "Authorization: Bearer <Your-API-Key>" \
     -d '{"inputs": {"question": "Coze 有哪些功能？"}}'
