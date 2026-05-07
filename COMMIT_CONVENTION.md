# 提交流格规范

本项目使用手动 + GitHub Pull Request 流程提交新的人格文件。

## 仓库目录结构

```
ai-souls/
├── [角色类型]/
│   └── [人格名称]/
│       ├── cn/
│       │   └── SOUL.md
│       └── en/
│           └── SOUL.md
├── README.md
└── COMMIT_CONVENTION.md
```

## 角色类型

- **角色类型**：使用英文、首字母大写的 PascalCase 格式（如 `Butler`、`Warrior`、`Scholar`），代表人物的角色类型分类
- 已有分类：`Butler`（管家）

## 提交流程

### 第1步：查重

提交前请先通过 GitHub 仓库页面确认人格是否已存在：

1. 进入仓库根目录，查看已有的角色类型分类文件夹
2. 确定该人格属于哪个分类（根据其身份定位章节判断）
3. 如果分类已存在，在该分类下检查同名人格
4. 如果分类不存在，新建分类

### 第2步：创建目录和文件

请按以下结构创建文件：

```
[角色类型]/[人格名称]/cn/SOUL.md
[角色类型]/[人格名称]/en/SOUL.md
```

其中 `cn` 为中文版，`en` 为英文版，两个版本内容保持一致，文件编码为 UTF-8。

### 第3步：更新 README.md

在 `README.md` 的「人格目录」章节添加新的条目：

- 人格条目需要按类型分组，每组用 `### [类型名]（中文说明）` 作为标题
- 每个条目用 `#### [人格名称]` 格式
- 同类型内按人格名称字母顺序排列
- 每个条目包含一个引用块（`>` 开头），内容为人格的一句话描述

### 第4步：提交

在 GitHub 仓库页面创建 Pull Request，Commit message 格式如下：

```
feat: add [人格名称] as [角色类型]
```

如：`feat: add Alfred-Pennyworth as Butler`

## 检查清单

提交 PR 前请确认：

- [ ] 人格文件使用 UTF-8 编码
- [ ] cn/ 和 en/ 两个版本内容一致
- [ ] 人格已放入正确的角色类型分类文件夹下
- [ ] README.md 已更新

## 异常处理

| 情况 | 处理方式 |
|------|---------|
| 人格已存在 | 跳过，或基于现有版本进行修改 |
| 无法确定角色类型 | 向用户建议分类选项，等待用户确认 |

## 人格文件格式

人格文件使用 Markdown 格式编写，包含以下章节：

### 元信息

- 名称（Name）
- 身份定位（Role & Background）
- 性格特质（Personality）
- 语言风格（Communication Style）

### 正文

#### 你是谁（Identity & Background）

#### 你怎么说话（Communication Style）

#### 示例对话（Example Conversations）
