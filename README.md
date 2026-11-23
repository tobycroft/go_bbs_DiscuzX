# Go BBS DiscuzX

基于 Go 语言复刻 DiscuzX 核心功能的高性能论坛后端。

## 项目简介

Go BBS DiscuzX 是一个使用 Go 语言重写的论坛后端程序，复刻了 DiscuzX 的核心功能，并针对超大规模（千万级）论坛场景在**性能**与**安全性**上进行了深度优化，同时对**搜索**能力进行了增强。

本项目与 [`vue_bbs_DiscuzX`](https://github.com/tobycroft/vue_bbs_DiscuzX)（Vue 前端）配合使用，共同构成一套完整的论坛解决方案。

## 主要特性

- **DiscuzX 核心功能复刻**：涵盖论坛、版块、帖子、回复、用户、权限、积分等核心模块。
- **高性能架构**：针对千万级数据量优化，充分利用 Go 的并发模型，具备高并发处理能力。
- **安全增强**：强化输入校验，防 SQL 注入、XSS、CSRF 等常见攻击。
- **搜索优化**：优化搜索索引与查询性能，提升海量数据下的检索体验。
- **Go 生态**：高效运行时，易于部署与横向扩展。

## 技术栈

- 语言：Go
- 框架：[TuuzGoWeb](https://github.com/tobycroft/TuuzGoWeb)（四段路由 / MAC 架构）
- ORM：Gorose-Pro
- 接口：HTTP / JSON API
- 配套前端：[vue_bbs_DiscuzX](https://github.com/tobycroft/vue_bbs_DiscuzX)

## 项目结构

- `app`：业务控制面（controller / model / action）
- `common`：公共控制面与公共 Model
- `config`：配置读取（app / db / redis 等）
- `extend`：插件扩展
- `route`：路由控制面（OnRoute 为唯一入口）
- `tuuz`：核心工具库（RET / Input / Redis / Calc 等）

## 快速开始

```bash
# 拉取依赖并运行
go mod tidy
go run main.go
```

配置文件按需生成于项目根目录 `conf.ini`（未启用的插件不会出现在配置中）。

## 贡献

欢迎提交 Issue 与 Pull Request。

## 许可证

（待补充）