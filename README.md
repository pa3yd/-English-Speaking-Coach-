# English Speaking Coach V1.0

交付为本地Skill与ChatGPT项目资料，非Web App，无付费API。默认训练先让用户说，模型通常只回复1–2句。

## ChatGPT项目使用
1. 新建个人项目，命名English Speaking Coach。把project_instructions.md正文粘贴到项目指令区，不只是上传它。
2. 解压交付包，上传chatgpt_upload中的01教练知识库.txt、02逐页课程.txt、03学习进度.json。资料包是纯文本/JSON，可直接逐个上传；不要只上传ZIP并假定已解析。
3. 发文字：“先说出BK5.0测试容量、ME循环流量与处理能力的区别，并指出来源。随后只问我一个基线口语问题。”确认资料可读后，再开始训练。
4. 如果你的项目界面提供语音或Live入口，在同一项目聊天开启；说：“今天练公司介绍。先让我说，你每次只说一两句。”若没有入口或语音不能读取资料，用文字训练，或把本课关键词和项目指令粘贴到可用语音聊天。
5. 结束时说：“结束训练，给出证据总结和新版progress.json。”保存快照，核对revision并替换上传的旧进度，避免多个最新版本并存。下一次开聊先提供最新快照；项目记忆不能替代进度文件核对。

当前账户Live、语音实际可用性、文件访问与进度持久化未实测。官方资料只支持项目共享上下文及可用语音能力的一般说明，不证明本Skill已经导入Live。没有自动导入或同步机制。

## Codex Skill
工作区根目录的SKILL.md是完整Skill入口，knowledge与presentation为相对引用。安装时复制到~/.codex/skills/english-speaking-coach；重新开启会话后用$english-speaking-coach调用，并确认读取本工作区progress.json。安装副本不是第二份学习日志。若在另一台电脑安装，复制本目录到该机器技能目录，修改SKILL.md中的规范进度路径。不要覆盖已有同名Skill或已有学习日志。

## 首次训练与验证
初始全部未评估；第一轮最多做自我介绍与一道客户问题。验证清单见VALIDATION_REPORT.md。不要把静态文件校验说成行为测试通过，也不要把语音已打开说成文件访问/学习记录已经验证。

## 来源和缺项
源文稿、PDF提取及逐条事实定位在knowledge；原PDF/PPT及已有练习稿不修改。未找到原始PPTX、讲者备注、可验证英语学习记录和旧教学提示词。日常英语场景为新教学建议；进度不预填历史。无可交付MP3；先前合成失败不算学习记录。

## 官方参考
- https://learn.chatgpt.com/docs/projects
- https://learn.chatgpt.com/docs/features/voice
- https://learn.chatgpt.com/docs/whats-new
核对日期2026-10-28。实际功能取决于账户与界面；未对用户项目执行上传或Live测试。
