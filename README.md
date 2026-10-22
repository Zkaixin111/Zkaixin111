<div align="center">

# 你好，我是张华 👋

**Java 后端 / AI 应用开发 · 2027 届 · 广州 / 深圳**

把大模型能力，做成稳定、可交付的工程系统。

[![Email](https://img.shields.io/badge/Email-2948631716@qq.com-red?logo=maildotru&logoColor=white)](mailto:2948631716@qq.com)
[![GitHub](https://img.shields.io/badge/GitHub-Zkaixin111-black?logo=github)](https://github.com/Zkaixin111)
![Status](https://img.shields.io/badge/状态-2027%20届求职中-2ea44f)

</div>

---

## 🧭 关于我

- 计算机科学与技术本科（2027 届），方向：**Java 后端 + AI 应用工程化**
- 独立完成 **5 个非模板项目**（从需求 → 建库 → 后端 → 前端 → 部署全流程），其中 **2 个 AI 全栈项目已部署上线，在线可体验**
- 关注的不是"AI 能生成什么"，而是**"怎么让它在工程上可控"**：多智能体编排、RAG 检索链路、SSE 流式推送、LLM 可观测
- 习惯给自己的系统做**评测与复盘**——先贤阁的几个 RAG 缺陷，都是跑评测集跑出来的，不是写代码时看出来的

### 🌐 在线演示（部署于阿里云 ECS：Docker + Nginx + systemd）

| 项目 | 地址 |
|---|---|
| 协笔 CoWrite | http://114.215.197.30:8080 |
| 先贤阁 | http://114.215.197.30:8090 |

---

## 🛠 技术栈

**后端**
![Java](https://img.shields.io/badge/Java-17%20%2F%2021-cc3524?logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-2.7%20%2F%203.x-6DB33F?logo=springboot&logoColor=white)
![Spring AI](https://img.shields.io/badge/Spring%20AI-Alibaba-6DB33F?logo=spring&logoColor=white)
![MyBatis](https://img.shields.io/badge/MyBatis--Plus%20%2F%20Flex-6DB33F)
![Sa-Token](https://img.shields.io/badge/Sa--Token-1.39-2ea44f)

**数据 / 中间件**
![MySQL](https://img.shields.io/badge/MySQL-4479A1?logo=mysql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?logo=redis&logoColor=white)
![RabbitMQ](https://img.shields.io/badge/RabbitMQ-FF6600?logo=rabbitmq&logoColor=white)
![Caffeine](https://img.shields.io/badge/Caffeine-本地缓存-8D2089)

**运维 / 部署**
![Docker](https://img.shields.io/badge/Docker-Compose-2496ED?logo=docker&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?logo=nginx&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-Ubuntu%2022.04-FCC624?logo=ubuntu&logoColor=white)
![Aliyun ECS](https://img.shields.io/badge/阿里云-ECS-FF6A00?logo=alibabacloud&logoColor=white)

**前端 / 客户端**
![Vue 3](https://img.shields.io/badge/Vue-3-4FC08D?logo=vuedotjs&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?logo=vite&logoColor=white)
![Electron](https://img.shields.io/badge/Electron-47848F?logo=electron&logoColor=white)

**自学中**
![Python](https://img.shields.io/badge/Python-自学-3776AB?logo=python&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain%20%2F%20LangGraph-自学-1C3C3C?logo=langchain&logoColor=white)

---

## 📌 项目矩阵

### 🖋 [协笔 CoWrite](https://github.com/Zkaixin111/zkx-ai-passage-creator) — Human-in-the-Loop AI 写作平台

针对「AI 一次性生成全文、结果不可控」的痛点，把创作重构为 **6 步可干预的智能体流水线**：标题、大纲、配图三个决策点暂停等用户确认，全程 SSE 实时推送进度。

`Spring Boot 3` `Spring AI Alibaba StateGraph` `SSE` `Vue3` `支付宝支付`

- 6 智能体编排为 5 段子图，**构造时一次编译缓存复用**；解决 OverAllState 深拷贝导致节点读不到更新的框架层问题
- 配图策略模式抽象 **6 种可插拔图源** + 三级降级链 + 双线程池并行，多图总耗时收敛为单图
- 商业闭环：VIP 配额单条原子 SQL 扣减、支付双端幂等（未支付订单复用 + 唯一索引 + 单向状态机）

### 🏛 [先贤阁](https://github.com/Zkaixin111/zkx-ai-sage-agent) — 多角色 RAG 问答与思辨平台

Spring AI Alibaba 全链路实践场：按角色隔离的 RAG 知识库检索、多轮对话记忆持久化、Function Calling 工具调用、思辨决斗场（多 Agent 定序辩论）与 LLM 可观测体系。

`Spring Boot 3.5` `pgvector` `RAG` `Function Calling` `Redis 多轮记忆`

- 自建 **30 题人工标注评测集**量化 RAG 效果，用相似度分布定位阈值根因、用真实会话日志反查拒答——三个缺陷都是评测跑出来的
- RAG 全链路：文档分片 → 向量入库 → 检索召回 → 重排 → 语义缓存，全程可观测

### 🖼 [拾光云图](https://github.com/Zkaixin111/zkx-java-picture) — 智能协同图库平台

公共 / 私有 / 团队三空间图片平台：AI 自动打标（分类 + 标签 + 主色调）、按颜色搜图、WebSocket 实时协同编辑。

`Spring Boot 2.7` `WebSocket + Disruptor` `RabbitMQ` `Caffeine + Redis 两级缓存` `Vue3`

- 异步 AI 打标：RabbitMQ 手动 ACK + 失败重入重试 + 死信队列兜底；生产环境排查过「模型名下线导致静默失败」并完成修复
- 上传链路：模板方法 + 策略模式双通道（文件 / URL 含 SSRF 防护），数据万象压缩 + 缩略图

### 🎬 [视频转换器](https://github.com/Zkaixin111/video-converter-desktop) — Electron 桌面应用

Windows 全离线桌面工具：8 种格式互转、FFmpeg **流直通零重编码**加速、批量任务队列、托盘常驻与崩溃恢复。

`Electron` `TypeScript` `FFmpeg` `Vue3`

### 🧪 [LangChain RAG 自学项目](https://github.com/Zkaixin111/LangChain-Agent-RAG-Project) — Python 线

LangChain 0.2 + LangGraph 0.2 + Chroma 的客服 RAG 小项目，用于理解 Python 生态的 Agent / RAG 实现，与我的 Java 线项目互为参照。

`Python` `LangChain` `LangGraph` `Chroma` `Streamlit`

---

## 📈 GitHub 统计

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=Zkaixin111&show_icons=true&hide_border=true&include_all_commits=true&count_private=true" height="150" alt="GitHub Stats" />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Zkaixin111&layout=compact&hide_border=true&langs_count=8" height="150" alt="Top Languages" />
</div>

---

## 🌱 成长规划

**进行中**
- 🔭 给先贤阁的 RAG 链路补评测体系：评测集扩充 + bad case 归因闭环（检索问题还是生成问题，分层定位）
- 📊 打磨 LLM 可观测：Token 成本核算、耗时分布、错误率统计，让每次模型调用都可解释

**计划中**
- 📝 把两个核心 AI 项目的「踩坑复盘」整理成系列文章（OverAllState 深拷贝、SSE 内存治理、模型名下线事故……）
- 🤝 从阅读源码开始参与 [Spring AI Alibaba](https://github.com/alibaba/spring-ai-alibaba) 社区：先提 issue、修文档，再尝试 PR
- ⚙️ 补齐 Java 基本功纵深：JVM 调优实践、分布式一致性场景

**一句话**

> 大多数人做完项目就结束了；我会反过来给自己的系统做评测，让下一个版本有据可依。

---

<div align="center">

如果我的项目对你有帮助，欢迎 Star ⭐ 交流 😊

</div>
