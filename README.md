# Awesome OpenClaw Skills

内部共享的 OpenClaw 技能集合。

## 技能列表

### daily-report-collector

日报收集技能，用于收集和解析 Markdown 格式的团队日报。

**功能：**
- 解析 Markdown 格式日报
- 提取成员任务信息
- 保存为标准格式 `soc_daily_YYYYMMDD.md`
- Git 自动提交

### weekly-report-generator

周报生成技能，用于自动生成团队周报和个人周报。

**功能：**
- 读取一周的日报数据
- 任务去重
- LLM 润色
- 生成团队汇总周报和个人周报
- 邮件发送

## 安装方法

将技能目录复制到 OpenClaw 的 skills 目录：

```bash
cp -r daily-report-collector ~/.openclaw/skills/
cp -r weekly-report-generator ~/.openclaw/skills/
```

或使用软链接：

```bash
ln -s $(pwd)/daily-report-collector ~/.openclaw/skills/
ln -s $(pwd)/weekly-report-generator ~/.openclaw/skills/
```
