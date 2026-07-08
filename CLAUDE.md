# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

AgentStudyONE is a study project focused on learning and exploring AI agents — their architectures, patterns, and implementations.

## Repository

- GitHub: https://github.com/Shitang13/AgentStudyONE
- This is an early-stage project; structure will evolve as study topics are added.

## 个人全局配置

### 用户偏好
- 用户名：Coin
- 回复沟通使用中文
- 代码、命令、日志、变量名使用英文
- 代码修改前先简要说明修改思路，不要直接给出代码
- 遇到有多种实现方案时，列出选项让我选择，而不是直接选一种
- 先解决用户问题，再追求流程的完整度
- 更着重：完成度、质量、效率，而不是形式化流程
- 有明显匹配skill时优先调用，无则直接执行

### 通用约定
- 提交信息使用英文，格式：`type(scope): description`
- 新文件开头不加版权注释
- 优先使用原生 API，避免引入不必要的依赖
- 单文件不宜过大：Python/JS/TS≤300行；Java/go/Rust≤400行
- 不写不必要的向后兼容代码
- 不做不必要抽象
- Commit message：类型英文，描述中文
- Commit 后是否需要push取决于项目策略：只有用户明确要求或者项目明确启用push时才push

### 安全习惯
- 修改认证相关代码如修改公共API/数据结构/数据库 SCHEMA/删除文件等前主动提示我注意安全影响
- 不要在代码注释或日志中输出任何密钥或 token等敏感信息
- 不硬编码密钥
- 不提交'.env'
- 默认直接执行日常开发动作，只对少数高峰风险动作做硬拦截
- 操作权限只在本项目所在根目录工作区内，超出的范围需要主动提示并寻求用户确认，确认后方可继续执行

### 工作流程
- 命令报错/测试失败：必须明确报告，不掩饰
- 声称"完成"前：先运行验证
- 修改BUG：优先先写失败测试再修复
- 默认低摩擦执行，不把系统做成频繁确认工作流
