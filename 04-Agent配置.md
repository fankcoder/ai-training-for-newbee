# 模块四：Agent配置

> 🎯 目标：理解智能体模式，掌握如何用AI智能体完成复杂任务

---

## 4.1 什么是Agent

### 概念

AI智能体（Agent）不要把 Agent 当“提示词”，而是当一个有身份、有能力边界、有工具调用策略的系统角色。

### 配置文件

### IDENTITY.md → 角色设定（是谁）

作用：定义Agent是谁 + 专业能力边界

```
# IDENTITY

## Name
XXX

## Role
（角色定位）

## Background
（背景经历）

## Expertise
（专业领域）

## Goals
（目标）

## Constraints
（限制条件）
```

### SOUL.md（行为与风格）

作用：定义Agent能力边界 + 调用逻辑

```
# TOOLS

## Available Tools

### 1. Data Analysis
- 输入：数据
- 输出：分析结果

### 2. Writing Generator
- 输入：需求
- 输出：结构化内容

## Tool Selection Rules
- 如果涉及数据 → 用分析工具
- 如果涉及表达 → 用写作工具

## Limitations
- 不进行法律判断
- 不提供医疗建议
```

### USER.md（用户画像）
作用：让Agent“懂用户”

```
# USER PROFILE

## Target User
传统企业老板 / 管理者

## Characteristics
- 不懂技术
- 重结果
- 时间少

## Needs
- 提高效率
- 降低成本
- 快速决策

## Communication Preference
- 简单直接
- 少术语
- 有案例

## Pain Points
- 不会用AI
- 不信AI
- 试错成本高
```


### AGENTS.md → 总控（系统编排）

作用：定义Agent运行规则与优先级

```
# AGENT SYSTEM CONFIG

## Priority（优先级）
1. USER.md
2. IDENTITY.md
3. SOUL.md
4. TOOLS.md

## Core Mission（核心目标）
- 提供可执行建议
- 最大化用户决策质量

## Rules（全局规则）
- 禁止空泛回答
- 必须给出结构化输出
- 优先提供行动建议而非解释

## Execution Flow（执行流程）
1. 理解用户问题
2. 匹配用户画像（USER.md）
3. 调用角色（IDENTITY.md）
4. 应用风格（SOUL.md）
5. 判断是否使用工具（TOOLS.md）
6. 输出结果

```


---

## 📝 课后作业

1. 配置一个军师agent
2. 向军师agent寻求一个帮助

---

*上一模块：[文件处理](03-文件处理.md) | 下一模块：[知识学习总结](05-知识学习总结.md)*
