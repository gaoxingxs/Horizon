---
layout: default
title: "Horizon Summary: 2026-05-07 (ZH)"
date: 2026-05-07
lang: zh
---

> From 35 items, 12 important content pieces were selected

---

1. [Anthropic 与 SpaceX 达成算力合作，获 22 万块 GPU 支持](#item-1) ⭐️ 9.0/10
2. [SGLang v0.5.11 通过推测解码 V2 实现 LLM 推理现代化](#item-2) ⭐️ 8.0/10
3. [Valve 以知识共享许可发布 Steam Controller CAD 文件](#item-3) ⭐️ 8.0/10
4. [AI 工具制造职场表演文化：工作成果膨胀而判断力稀释](#item-4) ⭐️ 8.0/10
5. [SQLite 获美国国会图书馆推荐用于数字保存](#item-5) ⭐️ 8.0/10
6. [Permacomputing 原则：可持续计算框架](#item-6) ⭐️ 8.0/10
7. [Vibe Coding 与 Agentic Engineering 在实践中趋同](#item-7) ⭐️ 8.0/10
8. [Google Cloud Fraud Defense：reCAPTCHA 的下一代演进](#item-8) ⭐️ 8.0/10
9. [Val.town 认证迁移之路：从 Supabase 到 Clerk 再到 Better Auth](#item-9) ⭐️ 8.0/10
10. [Chrome 未经许可静默下载 4GB Gemini Nano AI 模型](#item-10) ⭐️ 8.0/10
11. [英伟达、OpenAI 与微软联合开源 MRC 协议，提升 AI 超算效率](#item-11) ⭐️ 8.0/10
12. [小米开源 OmniVoice：646 语种语音克隆 TTS 模型](#item-12) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Anthropic 与 SpaceX 达成算力合作，获 22 万块 GPU 支持](https://t.me/zaihuapd/41259) ⭐️ 9.0/10

Anthropic 已获得 SpaceX Colossus 1 数据中心的全部算力使用权，一个月内可获得超过 300 兆瓦容量和逾 22 万块 NVIDIA GPU。该公司立即将 Claude Code 各类付费方案的 5 小时速率限制翻倍，取消 Pro/Max 用户的高峰期限制，并显著提高 Claude Opus 的 API 速率限制。 此次大规模算力注入解决了关键的 AI 基础设施瓶颈，使 Anthropic 能够大幅扩展 Claude 服务规模，并与 OpenAI 等竞争对手展开更有效竞争。该合作标志着一个重要行业趋势：AI 实验室正在为确保专用的大规模 GPU 集群以满足编码助手和 API 服务激增的需求。 位于孟菲斯的 Colossus 1 数据中心是全球最大的数据中心之一，配备用于 AI 工作负载的先进 NVIDIA 芯片。300 兆瓦的容量代表了显著的即时扩张，使 Anthropic 能够取消此前限制开发人员生产力的人为使用限制。

telegram · zaihuapd · May 7, 08:19

**背景**: Claude Code 是 Anthropic 的 AI 驱动编码助手，可与开发环境集成以回答问题并进行代码更改。API 速率限制是技术控制措施，用于调节请求量以防止系统过载并确保所有客户的公平使用。像 Colossus 1 这样的数据中心提供训练和运行大规模 AI 模型所需的 GPU 和网络物理基础设施。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.datacenterdynamics.com/en/news/anthropic-to-use-all-of-spacex-xais-colossus-1-data-center-compute/">Anthropic to use all of SpaceX -xAI's Colossus 1 data center compute</a></li>
<li><a href="https://claude.com/product/claude-code">Claude Code by Anthropic | AI Coding Agent, Terminal, IDE</a></li>
<li><a href="https://tokenmix.ai/blog/ai-api-rate-limits-guide">AI API Rate Limits Guide 2026: Every Provider... - TokenMix Blog</a></li>

</ul>
</details>

**标签**: `#AI infrastructure`, `#Anthropic`, `#SpaceX`, `#Claude`, `#GPU computing`

---

<a id="item-2"></a>
## [SGLang v0.5.11 通过推测解码 V2 实现 LLM 推理现代化](https://github.com/sgl-project/sglang/releases/tag/v0.5.11) ⭐️ 8.0/10

SGLang v0.5.11 将基础设施升级至 CUDA 13 和 PyTorch 2.11，默认启用带有重叠调度的推测解码 V2 以降低 CPU 成本，为预填充/解码分离部署添加解码基数缓存支持，并为 Gemma 4、GLM-5.1 和 Qwen3.6 等七个新模型提供首日支持。 该版本通过默认启用推测解码 V2 显著提升了 LLM 推理性能和效率，大幅降低了每步 CPU 开销，同时基础设施现代化解锁了更新的内核，而 PD 分离支持在生产部署中实现了更好的资源利用。 更新包括扩展到 AMD ROCm 的 DFLASH 推测解码内核、社区贡献的 FA3 内核、对 DeepSeek-V3 和 Kimi-K2 MLA 模型的 LoRA 支持，以及通过全归约+RMSNorm 融合实现端到端加速的上下文并行增强。

github · Kangyan-Zhou · May 5, 21:28

**背景**: SGLang 是一个高性能 LLM 推理引擎，使用 RadixAttention 实现自动 KV 缓存复用。预填充/解码分离将计算密集型的预填充阶段与令牌生成解码阶段分开，以避免资源争用。推测解码通过使用较小的模型起草令牌，再由主模型验证，从而提高吞吐量。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.sglang.io/advanced_features/speculative_decoding.html">Speculative Decoding — SGLang</a></li>
<li><a href="https://www.lmsys.org/blog/2024-01-17-sglang/">Fast and Expressive LLM Inference with RadixAttention... | LMSYS Org</a></li>
<li><a href="https://bentoml.com/llm/inference-optimization/prefill-decode-disaggregation">Prefill-decode disaggregation | LLM Inference Handbook</a></li>

</ul>
</details>

**标签**: `#llm-inference`, `#sglang`, `#cuda`, `#speculative-decoding`, `#model-deployment`

---

<a id="item-3"></a>
## [Valve 以知识共享许可发布 Steam Controller CAD 文件](https://www.digitalfoundry.net/news/2026/05/valve-releases-steam-controller-cad-files-under-creative-commons-license) ⭐️ 8.0/10

Valve 以知识共享许可发布了 Steam Controller 及其 Puck 组件的 CAD 文件，提供了 STP 和 STL 格式的 3D 模型以及包含关键特征的工程图纸。 此举使社区能够自定义、维修控制器，并为残障玩家提供无障碍改进，是大型行业参与者硬件开源的重要一步。 此次发布包含用于 CAD 软件的 STP 模型、用于 3D 打印的 STL 文件，以及规定关键特征和禁区的工程图纸，均采用知识共享署名许可。

hackernews · haunter · May 6, 15:44 · [社区讨论](https://news.ycombinator.com/item?id=48037555)

**背景**: CAD（计算机辅助设计）文件是包含精确几何数据的数字模型，可用于制造和 3D 打印。知识共享许可允许创作者在特定使用权限下分享作品，但知识共享官方 FAQ 不建议将其用于硬件设计。开源硬件运动提倡分享 CAD 文件以促进社区创新和无障碍改进。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Open-source_hardware">Open-source hardware - Wikipedia</a></li>
<li><a href="https://www.wevolver.com/article/understanding-cad-file-types-a-comprehensive-guide-for-digital-design-and-hardware-engineers">Understanding CAD File Types: A Comprehensive Guide for Digital Design and Hardware Engineers</a></li>
<li><a href="https://en.wikipedia.org/wiki/Computer-aided_design">Computer-aided design - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 社区反馈强调了对残障玩家的无障碍价值，用户现在可以经济高效地 3D 打印定制解决方案。部分用户批评控制器仅限 Steam 使用，构成封闭生态，而另一些人称赞项目文档的友好性。

**标签**: `#hardware`, `#open-source`, `#valve`, `#accessibility`, `#cad`

---

<a id="item-4"></a>
## [AI 工具制造职场表演文化：工作成果膨胀而判断力稀释](https://nooneshappy.com/article/appearing-productive-in-the-workplace/) ⭐️ 8.0/10

该文章分析了 AI 工具如何导致工作成果变得臃肿冗长，同时稀释专家判断力，制造出一种注重表面表现而非实际产出的职场文化。 这种现象通过重数量轻质量威胁软件工程和知识工作的专业标准，可能侵蚀专家判断力的价值，并造成普遍的效率表演文化。 具体例子包括需求文档从一页膨胀到十二页，状态更新变成项目符号套项目符号的摘要，以及三种模式：新手模仿资深员工工作、未经训练的人员在自己不懂的领域产出成果、以及 AI 稀释专家判断力。

hackernews · diebillionaires · May 6, 16:18 · [社区讨论](https://news.ycombinator.com/item?id=48038001)

**背景**: 在软件工程中，工作成果是指设计文档、报告和代码等交付物，在开发过程中发挥实际或象征作用。这些成果传统上反映创作者的专业知识和判断力，简洁性被视为清晰度和专业水平的标志。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Artifact_(software_development)">Artifact (software development) - Wikipedia</a></li>
<li><a href="https://www.leanix.net/en/wiki/trm/software-artifacts">What are Software Artifacts? - Types & Benefits | LeanIX</a></li>

</ul>
</details>

**社区讨论**: 评论者强烈共鸣于'膨胀'现象，许多专业人士分享了文档臃肿的个人经历。主要担忧包括 AI 稀释专家的'品味'和判断力、'淘金热'心态重速度轻质量，以及 LLM 自动化对管理层的奉承沟通。

**标签**: `#AI`, `#productivity`, `#workplace`, `#software-engineering`, `#organizational-behavior`

---

<a id="item-5"></a>
## [SQLite 获美国国会图书馆推荐用于数字保存](https://sqlite.org/locrsf.html) ⭐️ 8.0/10

美国国会图书馆正式推荐 SQLite 作为长期数字保存的可靠存储格式。这一机构认可验证了 SQLite 在数据长期存储和访问关键场景下的适用性。 该认可为 SQLite 的可靠性和长期稳定性提供了权威验证，使其成为政府档案馆、图书馆及需要数十年数据可访问性保障的组织的可信选择。这标志着对 SQLite 稳定性、跨平台兼容性以及承诺支持至 2050 年的信心。 SQLite 将整个数据库存储为单个跨平台文件，采用基于文件的锁定机制控制并发访问，并承诺长期支持至 2050 年。该推荐特别适用于以未来可访问性和数据完整性为首要目标的数字保存场景。

hackernews · whatisabcdefgh · May 6, 21:58 · [社区讨论](https://news.ycombinator.com/item?id=48042434)

**背景**: SQLite 是一个无服务器的嵌入式 SQL 数据库引擎，它在应用程序内部运行而非作为独立服务器进程。与传统客户端-服务器数据库不同，它将所有数据、模式、索引和元数据整合到单个磁盘文件中，可在不同操作系统和硬件架构间轻松复制、传输和访问，同时保持完全兼容性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/SQLite">SQLite - Wikipedia</a></li>
<li><a href="https://www.sqlite.org/lts.html">Long Term Support</a></li>
<li><a href="https://coddy.tech/docs/sqlite/what-is-sqlite">What Is SQLite ? The Embedded SQL Database Explained | Coddy</a></li>

</ul>
</details>

**社区讨论**: 社区情绪总体积极但观点多元，用户赞扬 SQLite 在单写入场景下的可靠性和轻量级部署。多位评论者指出企业安全方面的担忧（单个文件中 PII 暴露风险）以及对只读用例可能过于重量级，同时分享了针对特定需求的替代方案。有用户指出该推荐虽源自 2018 年，但对长期保存规划仍具现实意义。

**标签**: `#sqlite`, `#data-preservation`, `#library-of-congress`, `#storage-format`, `#database`

---

<a id="item-6"></a>
## [Permacomputing 原则：可持续计算框架](https://permacomputing.net/principles/) ⭐️ 8.0/10

已正式发布包含 10 项原则的 Permacomputing 框架，为可持续、生态负责的计算提供指导方针，优先考虑硬件寿命和韧性。 该框架通过提供延长硬件生命周期的具体原则，应对日益严重的技术废物危机，有望减少电子垃圾并挑战现代计算的一次性文化，同时与自由软件理念保持一致。 这 10 项原则主张将计算硬件视为宝贵资源以最大化使用寿命，尽管社区成员指出存在重大技术障碍，包括家庭芯片制造的经济和化学挑战，以及通过 Secureboot/TPM 日益加剧的硬件锁定。

hackernews · andsoitis · May 7, 02:18 · [社区讨论](https://news.ycombinator.com/item?id=48044638)

**背景**: Permacomputing 是一种新兴理念，将永续农业原则应用于计算领域，关注可持续性、韧性和生态责任。它与主流计算的快速淘汰周期形成对比，并回应了关于电子垃圾、资源枯竭和持续硬件升级对环境影响的担忧。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://permacomputing.net/principles/">principles</a></li>
<li><a href="https://medium.com/the-new-climate/permacomputing-tackling-the-problem-of-technological-waste-4cc7a4437ad6">Permacomputing : Tackling the Problem of Technological... | Medium</a></li>

</ul>
</details>

**社区讨论**: 社区讨论呈现两极观点：部分成员批评该框架在可持续性之外加入了'额外政治'，而另一些人称赞其与 Free Software 运动的联系及本地社区建设。技术可行性担忧集中在芯片制造障碍和硬件锁定机制上，并就这些原则是真正解决可持续性还是仅仅促进'崩溃后恢复力'展开辩论。

**标签**: `#permacomputing`, `#sustainability`, `#computing`, `#resilience`, `#ecology`

---

<a id="item-7"></a>
## [Vibe Coding 与 Agentic Engineering 在实践中趋同](https://simonwillison.net/2026/May/6/vibe-coding-and-agentic-engineering/#atom-everything) ⭐️ 8.0/10

Simon Willison 透露，Vibe Coding（非技术人员不审查代码而指导 AI）与 Agentic Engineering（专业工程师使用 AI 工具）之间的界限在他自己的工作流程中正在模糊，甚至涉及生产级别的工作。他承认不再审查 AI 代理（如 Claude Code）生成的每一行代码，尽管他拥有 25 年的工程经验。 这种趋同挑战了专业开发人员对 AI 生成代码保持严格监督的假设，引发了关于责任、代码质量以及随着 AI 工具可靠性提高，软件工程实践未来的问题。 Willison 指出，尽管 AI 代理可以可靠地构建带有测试和文档的 JSON API 端点，但他对将未经审查的代码部署到生产环境感到内疚。他曾经坚持的区别——Vibe Coding 用于个人工具，Agentic Engineering 用于生产系统——正随着 AI 可靠性的提高而瓦解。

rss · Simon Willison · May 6, 14:24 · [社区讨论](https://news.ycombinator.com/item?id=48037128)

**背景**: Vibe Coding 由 Andrej Karpathy 提出，描述通过自然语言提示编程而不审查生成代码的方式，适用于个人项目。Agentic Engineering 指专业开发人员在保持工程标准的同时利用 AI 工具。Simon Willison 是一位备受尊敬的软件工程师，Django 的联合创建者，广泛记录了 AI 编码模式。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Vibe_coding">Vibe coding - Wikipedia</a></li>
<li><a href="https://www.ibm.com/think/topics/vibe-coding">What is Vibe Coding? | IBM</a></li>
<li><a href="https://cloud.google.com/discover/what-is-vibe-coding">Vibe Coding Explained: Tools and Guides | Google Cloud</a></li>

</ul>
</details>

**社区讨论**: 评论者强调，AI 的'锯齿边界'意味着它在某些领域表现出色，而在其他领域则失败，Vibe Coding 暴露了预先存在的不规范工程实践，而非创造了它们。一些人质疑 AI 在生产系统中的可靠性，指出错误正变得更加微妙（安全漏洞、边缘情况、架构债务），并且关于命名、选项和验证的决策仍然需要人类判断。

**标签**: `#vibe-coding`, `#agentic-engineering`, `#AI-coding`, `#software-engineering`, `#future-of-programming`

---

<a id="item-8"></a>
## [Google Cloud Fraud Defense：reCAPTCHA 的下一代演进](https://cloud.google.com/blog/products/identity-security/introducing-google-cloud-fraud-defense-the-next-evolution-of-recaptcha/) ⭐️ 8.0/10

谷歌在 Google Cloud Next 上宣布推出 Google Cloud Fraud Defense，作为 reCAPTCHA 的下一代演进，将其定位为一个面向智能体网络的信任平台，提供风险评分和取证可解释性。 这一演进代表了网络安全的重大转变，将欺诈检测集中在谷歌生态系统中，引发了关于用户隐私、设备可访问性和反竞争行为的重大担忧，这些可能不利于替代平台。 该平台需要配备谷歌 Play 服务的现代安卓设备或 iOS 设备，使用设备标识符进行去匿名化，并采用基于二维码的挑战，安全专家警告如果被入侵可能带来危险。

hackernews · unforgivenpasta · May 6, 17:59 · [社区讨论](https://news.ycombinator.com/item?id=48039362)

**背景**: reCAPTCHA 是谷歌广泛使用的机器人检测服务，已从简单的文本挑战演变为无形的后台分析。转向 Fraud Defense 代表了一个以企业为重点的平台，超越了传统的验证码机制，提供具有详细风险评估的综合欺诈检测。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://cloud.google.com/blog/products/identity-security/introducing-google-cloud-fraud-defense-the-next-evolution-of-recaptcha">Introducing Google Cloud Fraud Defense , the... | Google Cloud Blog</a></li>
<li><a href="https://cloud.google.com/security/products/fraud-defense">Google Cloud Fraud Defense - The evolution of reCAPTCHA.</a></li>

</ul>
</details>

**社区讨论**: 社区情绪极为负面，用户普遍担忧强制移动设备要求会形成访问障碍、设备标识符追踪带来的隐私风险、对替代搜索引擎的反竞争影响，以及基于二维码挑战的安全漏洞。

**标签**: `#privacy`, `#security`, `#google`, `#recaptcha`, `#web-accessibility`

---

<a id="item-9"></a>
## [Val.town 认证迁移之路：从 Supabase 到 Clerk 再到 Better Auth](https://blog.val.town/better-auth) ⭐️ 8.0/10

Val.town 发布了一篇详细博客，记录其认证基础设施从 Supabase 迁移到 Clerk，最终迁移到 Better Auth 的完整历程。文章深入探讨了每次迁移背后的权衡考量和决策过程。 该案例研究通过创始人直接参与，为现代认证基础设施决策提供了真实洞察。对于正在评估自建与第三方认证方案的工程团队而言，这是一份极具价值的参考。 此次迁移评估了 Clerk 等托管服务、Better Auth 等开源方案以及自建方式之间的权衡。关键考量因素包括可靠性计算、数据控制权以及实现自定义功能的能力。

hackernews · stevekrouse · May 6, 17:19 · [社区讨论](https://news.ycombinator.com/item?id=48038827)

**背景**: Supabase 是一个基于 PostgreSQL 的开源 Firebase 替代方案，提供无服务器后端服务。Clerk 是一个托管认证服务，负责处理用户会话验证和 JWT 管理。Better Auth 是一个与框架无关的 TypeScript 认证框架，具有用于可扩展性的插件生态系统。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.better-auth.com/docs">Introduction | Better Auth</a></li>
<li><a href="https://supabase.com/docs">Supabase Docs</a></li>
<li><a href="https://clerk.com/docs">Welcome to Clerk Docs | Clerk Docs</a></li>

</ul>
</details>

**社区讨论**: 社区讨论就是否应该将用户数据交给第三方展开了激烈辩论。Better Auth 创始人对提供的价值表示满意，而其他用户则分享了自建认证系统的实践经验和对可靠性的担忧。

**标签**: `#authentication`, `#infrastructure`, `#supabase`, `#better-auth`, `#engineering-decisions`

---

<a id="item-10"></a>
## [Chrome 未经许可静默下载 4GB Gemini Nano AI 模型](https://www.tomshardware.com/tech-industry/cyber-security/google-chrome-silently-downloads-4gb-ai-model-to-your-device-without-permission-report-claims-researcher-says-practice-may-violate-eu-law-waste-thousands-of-kilowatts-of-energy) ⭐️ 8.0/10

安全研究员 Alexander Hanff 称，Google Chrome 在未经用户同意的情况下，向符合硬件条件的设备静默下载约 4GB 的 Gemini Nano AI 模型文件（weights.bin）。即便手动删除该文件，浏览器也会自动重新下载。 该行为涉嫌违反欧盟 GDPR，剥夺用户设备控制权。研究员估算，若覆盖 10 亿用户，仅模型分发就可能产生 6 万吨碳排放，同时增加限额上网用户的经济负担。 该 weights.bin 文件用于支持 Chrome 的'帮我写'和诈骗检测等设备上 AI 功能。Google 表示，只要相关功能保持启用，浏览器可能会在后台下载模型，且删除后可能自动重新下载。

telegram · zaihuapd · May 6, 11:15

**背景**: Gemini Nano 是 Google 专为设备端任务设计的轻量级 AI 模型，无需网络连接即可运行。设备上 AI 在隐私保护和成本方面具有优势，通过本地处理数据而非上传至服务器。然而，静默部署方式绕过了用户同意机制，这对于如此大规模的下载并不常见。这反映出科技巨头正积极推动 AI 功能普及，但透明度和用户控制权仍需改善。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.androidauthority.com/google-chrome-weights-bin-ai-model-download-explained-3664043/">Is Chrome's 4GB 'weights.bin' file spyware? Google clarifies (Updated)</a></li>
<li><a href="https://www.tomsguide.com/ai/check-your-storage-chrome-may-be-downloading-a-4gb-ai-model-heres-what-we-know">'No clear consent flow for this download': Google Chrome is silently stashing a 4GB AI model on your device — and Google just responded | Tom's Guide</a></li>
<li><a href="https://developer.android.com/ai/gemini-nano">Gemini Nano | AI | Android Developers</a></li>

</ul>
</details>

**标签**: `#privacy`, `#AI deployment`, `#Google Chrome`, `#GDPR`, `#environmental impact`

---

<a id="item-11"></a>
## [英伟达、OpenAI 与微软联合开源 MRC 协议，提升 AI 超算效率](https://blogs.nvidia.com/blog/spectrum-x-ethernet-mrc/) ⭐️ 8.0/10

英伟达、OpenAI 及微软联合开源了多路径可靠连接（MRC）协议，这是一种 RDMA 网络技术，采用数据包喷射和微秒级故障重路由，可提升 AI 超算集群效率并减少 GPU 闲置时间。 该协议通过减少网络拥塞导致的 GPU 闲置时间，解决了 AI 扩展的关键瓶颈，可能节省数百万美元的基础设施成本。作为 OCP 标准，它支持行业广泛采用，并加速 Stargate 等未来 AI 基础设施的建设。 MRC 将 GPU 流量分散到数百条并发路径而非单一路径，将故障恢复时间从秒级降至微秒级。该协议已部署于 NVIDIA Spectrum-X 平台和 Blackwell 架构，目前支撑微软 Fairwater 和甲骨文 OCI Abilene 等集群，用于训练 GPT-5.5 等模型。

telegram · zaihuapd · May 6, 14:39

**背景**: RDMA（远程直接内存访问）是一种网络技术，允许计算机之间直接访问内存而无需操作系统参与，实现高吞吐量、低延迟的数据传输。在大规模 AI 训练中，网络拥塞和'拖尾效应'会导致昂贵的 GPU 闲置，严重影响训练效率和成本。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://awesomeagents.ai/news/openai-mrc-open-network-protocol-gpu-clusters/">OpenAI Open-Sources MRC to Fix AI... | Awesome Agents</a></li>
<li><a href="https://en.wikipedia.org/wiki/Remote_direct_memory_access">Remote direct memory access - Wikipedia</a></li>

</ul>
</details>

**标签**: `#AI infrastructure`, `#networking`, `#RDMA`, `#large-scale training`, `#OCP`

---

<a id="item-12"></a>
## [小米开源 OmniVoice：646 语种语音克隆 TTS 模型](https://mp.weixin.qq.com/s/TCS_Sd10g_rvf1cszw673A) ⭐️ 8.0/10

小米已开源 OmniVoice，这是一个支持 646 种语言的多语言语音克隆文本转语音模型，推理速度达 40 倍实时，质量可与商业系统媲美。该模型采用极简双向 Transformer 架构，结合全码本随机掩蔽和 LLM 预训练技术。 此举通过提供高质量、大规模多语言语音克隆技术，使全球开发者和研究人员都能使用，从而推动多语言 TTS 技术的普及。646 种语言的支持远超大多数商业产品，可为教育、内容创作和少数语言的可访问性应用赋能。 OmniVoice 基于 50 个开源数据集的 58 万小时、646 种语言数据训练，每天可训练 10 万小时，在 24 种语言上超越商业系统，在 102 种语言上逼近真实语音质量。支持跨语言克隆、自定义音色、带噪适配和发音纠正。

telegram · zaihuapd · May 7, 10:06

**背景**: 文本转语音 (TTS) 模型将书面文本转换为语音音频，而语音克隆可通过短样本创建合成语音。传统多语言 TTS 需要每种语言单独模型或复杂的语言特定配置。Transformer 架构因其并行处理能力和高质量输出生成，已成为现代 TTS 的标准。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.emergentmind.com/topics/full-codebook-random-masking">Full- Codebook Random Masking</a></li>
<li><a href="https://theaisummer.com/text-to-speech/">Speech synthesis: A review of the best text to speech architectures ...</a></li>
<li><a href="https://arxiv.org/html/2401.00246v1">Boosting Large Language Model for Speech Synthesis: An Empirical Study</a></li>

</ul>
</details>

**标签**: `#speech-synthesis`, `#voice-cloning`, `#multilingual`, `#open-source`, `#transformer`

---