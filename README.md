# Awesome OpenClaw Skills

内部共享的 OpenClaw 技能集合。

## 开发工作流

| 技能 | 用途 |
|------|------|
| project-manager | 项目管理、需求拆分、任务分配、进度统计 |
| architect | 系统架构设计、模块划分、通信协议定义 |
| git | 版本控制、代码备份和同步 |

## 开发者

| 技能 | 用途 |
|------|------|
| developer | 通用开发者，根据架构文档实现功能代码 |
| backend-developer | Python 后端开发，FastAPI/Flask、RESTful API |
| frontend-developer | Web 前端开发，React/TypeScript、Tailwind CSS |
| unreal-developer | Unreal Engine C++ 开发，UE5 代码规范 |

## 测试

| 技能 | 用途 |
|------|------|
| qa | 测试专家，单元测试 + 冒烟测试 |
| llt-qa | UE5 单元测试，Catch2 框架，CI 友好 |
| gauntlet-qa | UE5 整合测试，Gauntlet Framework，端到端验证 |

## 调试

| 技能 | 用途 |
|------|------|
| debug | 调试专家，嵌入调试日志，问题定位 |

## 报告

| 技能 | 用途 |
|------|------|
| daily-report-collector | 日报收集，解析 Markdown 格式团队日报 |
| weekly-report-generator | 周报生成，任务去重 + LLM 润色 + 邮件发送 |

## 安装方法

将技能目录复制到 OpenClaw 的 skills 目录：

```bash
cp -r * ~/.openclaw/skills/
```

或使用软链接（便于 git pull 更新）：

```bash
for skill in */; do ln -s $(pwd)/$skill ~/.openclaw/skills/; done
```
