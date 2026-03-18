# 团队周报 - 20260302（分类修复版）

## 📊 分类统计（修复后）

| 分类 | 任务数 | 占比 |
|------|--------|------|
| CI/构建系统 | 31 | 41.3% |
| 未分类 | 25 | 33.3% |
| 鸿蒙平台 | 7 | 9.3% |
| 工具开发 | 6 | 8.0% |
| 内存优化 | 3 | 4.0% |
| 音频系统 | 2 | 2.7% |
| 资源系统 | 1 | 1.3% |

**总计**: 75 个任务

## 📋 分类任务详情

### CI/构建系统

- 查找bug原因 #107421 【基建专项】【publish分支】安卓端包体下载资源完成后界面卡死在正在准备加载资源1%，等待几分钟后会闪退 http://soc-redmine.wd.com/issues/107421 _[fixed]_
- 流水线打出来的publish asan包 还有问题 _[fixed]_
- code_version修复问题打包验证。 _[fixed]_
- 查看骑士装备购买crash问题文档 _[fixed]_
- weekly打包crash问题（已找到原因能成功打包） _[fixed]_
- 引擎公告编码问题修复 _[fixed]_
- 调查android准备资源1%卡住后crash，上次时复现是由于本地patch执行与ci不同导致，改成相同后没法复现，只能等下次再出现时查 _[fixed]_
- audio crash问题查看，可能是外挂或云游戏 _[fixed]_
- Texture泄露相关基本完成, 等poco修复后再给一版自动化的泄露报告 _[fixed]_
- 体验分支安卓打包失败调查(最后一次打包仍失败还需调查) _[fixed]_
- 修复#107890 【建造系统】【领地中枢】【偶现】玩家起床后观察到已激活情报模式的情报柜显示的是领地柜模式，需要过一会才会正常显示为情报柜模型 http://soc-redmine.wd.com/issues/107890 _[fixed]_
- publish asan问题，让asan流水线关闭反作弊，重新出包，明天待QA验收 _[fixed]_
- 为了适配hwasan流水线，修改打包脚本 _[fixed]_
- 安装Intel VTune, 测试遇到crash _[fixed]_
- 开始实现代码，获取了客户端版本查找代码版本的接口，剩余符号加载和测试 _[fixed]_
- 断线重连时的版本检测问题修复 _[fixed]_
- 引擎暴露回调接口监控LoadAllAssetsAtPath的调用 _[fixed]_
- 编辑器插件注册回调, 回调条件触发卸载资源 _[fixed]_
- 骑士包crash文档查看与复现环境搭建 _[fixed]_
- 协助杨阳符号服务器（15%的时间） _[fixed]_
- mmap新版打包配置修改 _[fixed]_
- 体验分支安卓打包失败调查(已删除library依旧失败，同一版本本地能正常打，打包机不行) _[fixed]_
- publish asan流水线关掉反作弊，仍然挂在libtersaf.so。尝试把反作弊相关代码用宏包起来看看 _[fixed]_
- 骑士包crash的问题复现与原因确认，额外确认了Editor为什么不会OOB。目前进度：正在本地打包引擎测试。 _[fixed]_
- 继续调查体验分支安卓打包失败问题（仍然失败，预计重新拉个工程） _[fixed]_
- trunk_oversea流水线排查：启动参数设置问题（已修改）-enableGoogle true -enableFacebook true -enableApple true；asset pack路径不存在，疑似跟streamingAssets下载列表的bundle下载失败导致 _[fixed]_
- 查看crashSight提供的接口功能，确定组合方案：先根据日期批量获取crash信息，再根据id尝试下载附件内容，完成代码实现；调试接口时，发现接口行为和预期不符，记录问题并询问crashsight接口人 _[fixed]_
- 打包assetbundle自动上传shader信息 _[fixed]_
- 平台资源生成从30+GB降到10+GB _[fixed]_
- 协助杨阳解决部分符号服务器问题(10%) _[fixed]_
- 骑士包crash问题，编译引擎打包测试。 _[fixed]_

### 未分类

- Hotfix成功上传TLog _[fixed]_
- 补充rename规则，以及新规则相应的测试用例TestCase21、TestCase22，测试用例已跑通 _[fixed]_
- 收集需要上传哪些符号文件，完成了文档：https://alidocs.dingtalk.com/i/nodes/vy20BglGWOerz5AgSGrwodNrJA7depqY _[fixed]_
- 服务器创建了共享目录，创建了windows账户并配置了相关权限，本地成功测试上传文件 _[fixed]_
- 多语言hotfix热更已测试完毕 _[fixed]_
- 配合腾讯风险组件调查 _[fixed]_
- 组内会议 _[fixed]_
- trunk长线跑测崩溃 _[fixed]_
- 编辑器下清理动画变体的脏数据 引擎部分实现测试通过已提交 _[fixed]_
- 为利用现有的符号备份，确定bat方式的可行性，执行后自动配置可用的符号路径；手动创建dmp测试，了解学习该流程相关知识，并记录疑问 _[fixed]_
- trunk长线跑测崩溃 - 跟进 - 最初测试QA尚无后续反馈(待机，等待最新信息反馈中) _[fixed]_
- Package&Tag设置相关信息答疑 - 计划外(0.5h) _[fixed]_
- Rename成对匹配测试通过，能正常拦截或放行 _[fixed]_
- 确定了bat添加符号方案流程，以及需要完成的内容 _[fixed]_
- shader预热文档整理 _[fixed]_
- 测试build client会死锁, 还在调查原因 _[fixed]_
- 体验服配置结构沟通实现（完成） _[fixed]_
- hotfix下载失败后，重试下载修改 _[fixed]_
- 地图Package & Tag设置答疑 - 计划外 - 0.5h _[fixed]_
- 架构组周会 - 1h _[fixed]_
- dev包gc测试数据导出异常排查 _[fixed]_
- 复制文件夹 A → 删除原文件夹 A → 将副本改名回 A，分析完成，具体看文档https://alidocs.dingtalk.com/i/nodes/vy20BglGWOerz5AgSG2vzd1ZJA7depqY 场景4 _[fixed]_
- 查看后台默认下载的方案相关文档，了解相关内容 _[fixed]_
- 文件服shader信息合并 _[fixed]_
- 效果 BuildClient从40+GB降到10+GB _[fixed]_

### 鸿蒙平台

- 检查是否没有运行到播放音频的代码，增加声音播放的测试代码，方便打包鸿蒙apk真机测试声音是否正常（已完成） _[fixed]_
- 升级鸿蒙相应资产打包流水线（已完成） _[fixed]_
- 鸿蒙 - Ab打包疏通 _[fixed]_
- 鸿蒙引擎 android ab打包问题排查。 _[fixed]_
- 鸿蒙 - Ab打包疏通 - 跟进 - 今天暂无内容跟进 _[fixed]_
- 鸿蒙 - Ab打包疏通 - 跟进 - 李晓夫反馈鸿蒙Ab打包失败 - 8h(持续排查中) _[fixed]_
- 协助解决鸿蒙AB打包，及下载问题(15%) _[fixed]_

### 工具开发

- 校对引擎发布分支信息以及确认新需求（需要增加引擎git版本查询供qa使用） _[fixed]_
- 引擎历史查询工具优化 已支持打包输出版本号对应查找以及界面直接fix所有版本信息 _[fixed]_
- 完成符号自动部署脚本(bat及py),包含：传入版本号，自动下载对应符号解压；成功自动关联VS符号配置路径；拆分版本号查询功能，支持根据版本号获取代码提交信息等。 _[fixed]_
- 新增引擎git提交记录查询工具 _[fixed]_
- shader进包变体editor查询工具 _[fixed]_
- editor下材质shader变体查看工具 _[fixed]_

### 内存优化

- 开始回头搞打包内存高的问题, 先把环境搭起来 _[fixed]_
- 搞打包内存高的问题 确定一版方案 _[fixed]_
- 搞打包内存高的问题 _[fixed]_

### 音频系统

- 开始排查PC asan版本音频crash _[fixed]_
- #105305 [音频]需要排查音频调用接口 _[fixed]_

### 资源系统

- mmap文件压缩 进度：3900+动画mmap文件已压缩至40个文件+1个manifaset映射文件 文件数量可以通过实际测试后的解压速度再减少，目前单个文件在2M～11M。 编辑器测试已通过。 准备提交打包测试：看是直接提交trunk还是在其他分支先测试。适配了单个文件加载的逻辑不会引起无法加载的情况。 _[fixed]_

---
*此分类周报由自动化系统生成（修复版）*