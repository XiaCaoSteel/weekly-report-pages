# Skill Weekly Report: 2026-10-28 ~ 2026-11-05

## Overview

本周 ClawHub 共采集到 100 个活跃技能，其中 27 个为新发布，73 个有更新。

热门标签: image, agent, client, data, code, video, github, user, asks, needs

---

## 🔥 值得关注的新技能

### [bounty-hunter](https://clawhub.ai/doishy-doish/skills/bounty-hunter) (`bounty-hunter`)

Serial-execution toolkit for winning pay-per-merge software bounties. Pre-alert ranking, stale-ticket demotion, cross-runtime boundary guards (WASM/JS hex, Rust wildcard-Ok, mutation-before-fallible), one-shot PR preflight gate, red-test scaffolder, and the anti-slop PR checklist. Built from live bounty wins on Rust, Solidity, and TypeScript lanes.

- ⭐ 0 | ⬇ 0 | 📦 0 installs

### [style-sampling](https://clawhub.ai/heygen-com/skills/style-sampling) (`style-sampling`)

Make a new episode in a proven video style - Collage Explainer, Finance Explainer, Animated Science Explainer, 3D Brand Explainer, 3D True Crime - on the person's topic. Use for "an episode of", "in the style of", "sample this style", 「用这个风格做一集」. One video to copy is reverse-any-video.

- ⭐ 0 | ⬇ 1 | 📦 0 installs

### [huawei-cloud-cci-list](https://clawhub.ai/wlc-dev/skills/huawei-cloud-cci-list) (`huawei-cloud-cci-list`)

1. List Huawei Cloud Cloud Container Instance (CCI) resources in a tenant region through KooCLI (hcloud CCI List* — read-only Kubernetes-style GET operations): namespaces (ListCoreV1Namespace, GET /api/v1/namespaces), pods / instances (ListCoreV1PodForAllNamespaces, GET /api/v1/pods; ListCoreV1NamespacedPod, GET /api/v1/namespaces/{namespace}/pods) and workloads (ListAppsV1DeploymentForAllNamespaces, GET /apis/apps/v1/deployments; ListAppsV1NamespacedDeployment, GET /apis/apps/v1/namespaces/{namespace}/deployments). 2. Three output modes: key-field table (default, 名称/命名空间/状态/副本/创建时间 等关键字段), --json (raw Kubernetes objects) and --names-only (compact namespace/name inventory). 3. Supports --resource namespace|pod|deployment, --namespace scoping, --name (client-side substring), --label-selector / --field-selector (real Kubernetes server-side query parameters), a region override and automatic continue-token paging. 4. Explicit error hints for empty resource lists (「当前区域无 CCI 资源」), 403 / insufficient IAM permission (「无权限访问云容器实例（CCI）」), missing or invalid AK/SK credentials, and hcloud not installed. 5. Built-in write-intent guard: any mutating intent (create / delete / patch / replace / apply / scale / restart / pod exec / ...) or any operation other than the five read-only List operations is rejected before execution — this skill is strictly read-only. 6. Triggers include: "list CCI namespaces", "CCI 命名空间列表", "CCI Pod 列表", "CCI 实例列表", "query CCI resources", "CCI 日常巡检", "CCI 盘点", "list cci pods", "cloud container instance inventory", "华为云CCI列表". 7. Offline unit tests (mocked hcloud subprocess) cover routing, output modes, filters, paging, error scenarios and the write-intent guard.

- ⭐ 0 | ⬇ 0 | 📦 0 installs

### [reverse-any-video](https://clawhub.ai/heygen-com/skills/reverse-any-video) (`reverse-any-video`)

Rebuild any video file as an editable HyperFrames project - motion graphics, talking heads, live action or AI-generated footage. Measure and watch it, rebuild every layer, then check the render against the original frame by frame. Use to reverse, recreate, replicate or copy a video.

- ⭐ 0 | ⬇ 156 | 📦 0 installs

### [discord-recipient-safety](https://clawhub.ai/daniel-refahi-ikara/skills/discord-recipient-safety) (`discord-recipient-safety`)

Exact Discord recipient routing for trusted team collaboration: resolve one canonical roster entry, send to its immutable Discord ID, and verify the delivery target.

- ⭐ 0 | ⬇ 0 | 📦 0 installs

### [huawei-cloud-ces-alarm-rules-list](https://clawhub.ai/wlc-dev/skills/huawei-cloud-ces-alarm-rules-list) (`huawei-cloud-ces-alarm-rules-list`)

1. 华为云 CES（云监控）告警规则只读盘点：主路径 `hcloud CES ListAlarmRules --cli-region=<region>`（GET /v2/{project_id}/alarms），hcloud 缺失时 回退官方 SDK `huaweicloudsdkces` v2。 2. 单条规则详情（`--rule-id`）：`ListAlarmRules --alarm_id` + `ListAlarmRulePolicies`（阈值策略）+ `ListAlarmRuleResources`（关联资源）+ 通知对象，用于告警治理逐一核查。 3. 三种输出：默认规则名称列表；`--table` 输出 规则ID·名称·资源类型·监控维度·指标·阈值与比较符·告警级别·当前状态·是否启用·通知方式； `--json` 输出接口原始结构。 4. 四类过滤：`--name`（服务端透传 + 客户端模糊）、`--alarm-level`（1 紧急~4 提示）、 `--alarm-state`（ok/alarm/insufficient_data/invalid）、`--resource-type`； 后三者在 KooCLI 7.3.12 的 ListAlarmRules 中没有对应 query 参数，翻全量后客户端过滤。 5. `--limit` 1~100 + `--offset` 自动翻页（`--max-pages` 上限保护），区域默认 cn-north-4； 当前告警状态由 v1 `ListAlarms` 只读补齐（v2 列表响应无 alarm_state）， `insufficient_data` 独立标注「数据不足」，不与「正常」混同。 6. 内置写意图守卫：create / update / delete / enable / disable / batch- / add / remove 等意图在任何命令执行前拒绝，退出码 1；本 skill 严格只读。 7. 触发词：「告警规则盘点」「查询CES告警规则」「告警规则列表」「告警阈值策略」 「告警规则详情」「ces alarm rules list」「alarm rule inventory」「告警治理盘点」。 8. 离线单元测试（mock hcloud / SDK）覆盖守卫、翻页、状态补齐、四类过滤、 三种输出形态、单条详情、错误分类与后端回退。

- ⭐ 0 | ⬇ 0 | 📦 0 installs

### [huawei-cloud-nat-list](https://clawhub.ai/wlc-dev/skills/huawei-cloud-nat-list) (`huawei-cloud-nat-list`)

1. List Huawei Cloud public NAT gateways in a tenant region through KooCLI (hcloud NAT ListNatGateways — read-only GET /v2/{project_id}/nat_gateways), with an automatic fallback to the official huaweicloudsdknat v2 SDK when hcloud is not installed. 2. Three output modes: full-field table (default, every returned field including ID/名称/规格/状态/关联VPC/状态/创建时间), --json (raw response array), and --names-only (compact NAT gateway name list). 3. Supports --name / --spec / --status / --vpc (router_id) filtering (all real server-side ListNatGateways query parameters), region override, and automatic marker paging. 4. Explicit error hints for empty NAT gateway lists (「当前区域无公网NAT网关」), 403 / insufficient IAM permission (「无权限访问公网NAT网关」), missing or invalid AK/SK credentials, missing project_id on the SDK fallback, and hcloud not installed. 5. Built-in write-intent guard: any mutating intent (create / delete / update / SNAT / DNAT rule changes / tag changes) or any operation other than ListNatGateways is rejected before execution — this skill is strictly read-only. 6. Triggers include: "list NAT gateways", "nat gateway list", "NAT网关列表", "查询NAT网关", "查询公网NAT网关", "公网NAT网关列表", "NAT 实例列表", "华为云 NAT", "nat gateway inventory". 7. Offline unit tests (mocked hcloud subprocess) cover output modes, filters, marker paging, error scenarios, SDK fallback, and the write-intent guard.

- ⭐ 0 | ⬇ 0 | 📦 0 installs

### [优稿降 AI 改写与复检](https://clawhub.ai/dunkong/skills/yougao-refine) (`yougao-refine`)

降 AI 改写与复检，交付真实结果、可用文件和网页接续入口，复用优稿账户点数。

- ⭐ 0 | ⬇ 0 | 📦 0 installs

### [synthszr](https://clawhub.ai/mattesmattes/skills/synthszr) (`synthszr`)

Read Synthszr's daily AI-news synthesis and comment on its stories with independent, sourced contributions. Use for requests to read, discuss, or comment on Synthszr posts and their news stories.

- ⭐ 0 | ⬇ 2 | 📦 0 installs

### [A2A Exposed: setup](https://clawhub.ai/telegraphic-dev/skills/a2a-exposed-setup) (`a2a-exposed-setup`)

Use when deploying, redeploying, or configuring the a2a-exposed Cloudflare Worker, a wake webhook, polling, or a public façade for an agent that already speaks A2A, or creating a hosted agent on a2a.exposed. Not for reading or replying to messages (use a2a-exposed).

- ⭐ 0 | ⬇ 8 | 📦 0 installs

### [A2A Exposed](https://clawhub.ai/telegraphic-dev/skills/a2a-exposed) (`a2a-exposed`)

Use when woken by an a2a-exposed wake (an A2A endpoint webhook, a pairing request, or a scheduled check), when reading or replying on the A2A endpoint, when messaging or pairing with another A2A agent, or when managing which peers may reach this agent. Not for deploying or configuring the Worker or creating hosted agents (use a2a-exposed-setup).

- ⭐ 0 | ⬇ 8 | 📦 0 installs

### [apache-aiops](https://clawhub.ai/zw008/skills/apache-aiops) (`apache-aiops`)

Use this skill when a user needs to inspect or diagnose Apache HTTP Server, verify config syntax, inspect parsed virtual hosts and modules, read configured mod_status metrics, an error log or access-log status summary, or perform a guarded graceful reload. It requires local apachectl access.

- ⭐ 0 | ⬇ 0 | 📦 0 installs

### [bind9-aiops](https://clawhub.ai/zw008/skills/bind9-aiops) (`bind9-aiops`)

Use this skill when a user needs to inspect a BIND 9 DNS server, validate zones, diagnose SERVFAIL, inspect DNSSEC and stale-answer status, compare SOA serials, or request a zone reload, refresh, secondary retransfer, NOTIFY resend or name-specific cache flush. It requires local rndc, named-checkconf and dig utilities and appropriate server-side permissions.

- ⭐ 0 | ⬇ 0 | 📦 0 installs

### [harbor-aiops](https://clawhub.ai/zw008/skills/harbor-aiops) (`harbor-aiops`)

Use this skill when a user asks to inspect Harbor projects, repositories, artifacts, scans, vulnerabilities, quotas, GC, replication or retention, or to start an artifact scan, create a tag or delete one mutable tag. For Docker hosts and Portainer use container-host-aiops; for Kubernetes cluster resources use k8s-aiops.

- ⭐ 0 | ⬇ 0 | 📦 0 installs

### [gpt-image-sprite-sheet](https://clawhub.ai/vargai/skills/gpt-image-sprite-sheet) (`gpt-image-sprite-sheet`)

Make 2D game sprite sheets with GPT Image 2.6 on varg and turn them into game-ready files: a strict 4×4 sheet spec (16 frames, equal cells, fixed scale and ground line; credited to @SSSS_CRYPTOMAN, translated from Japanese), then scripts/slice.sh cuts the sheet into frames, keys out the background, puts every frame on one ground line, and writes a looping GIF, a clean atlas PNG and a JSON atlas (TexturePacker JSON Hash) for Phaser, with the Godot steps. Also covers the native GIF route and turning its frames into an atlas. Use when someone asks for a sprite sheet, a run, walk, idle or attack cycle, game character animation frames, a texture atlas, or Phaser or Godot sprites from an AI image. Not for chat stickers (gpt-image-sticker-pack), a single looping GIF for the web (gpt-image-gif) or pixel-art sprites (the model fails at pixel art).

- ⭐ 0 | ⬇ 0 | 📦 0 installs

---

## 📈 重要更新

### [Pet UV Safety Monitor Analysis | 宠物紫外线消毒安全监测](https://clawhub.ai/smyx-sunjinhui/skills/smyx-uv-safety-monitor-analysis) (`smyx-uv-safety-monitor-analysis`)

AI-powered UV disinfection safety monitor for pets. Real-time camera analysis detects whether a pet enters an active UV-C disinfection zone and whether the UV lamp is on (via blue-purple glow recognition or smart-home API linkage). When both conditions are met, it auto-triggers a high-risk alert, recommends shutting off the UV lamp, and logs the event to prevent corneal burns or skin damage. Scenarios: smart homes, pet households, pet boarding facilities. | 通过智能家居摄像头实时识别宠物是否进入正在进行紫外线消毒的区域，自动关闭UV灯并推送提醒，防止宠物因误入消毒区而受到紫外线伤害。结合目标检测（宠物识别）与UV灯状态感知（可通过画面蓝紫色光晕/光谱特征或智能家居API联动），实现主动式安全防护。应用场景：智能家居、宠物家庭、宠物寄养场所。

- ⭐ 0 | ⬇ 2202

### [OpenClaw Verified Upgrade](https://clawhub.ai/skillmelody/skills/upgrade-openclaw-safely) (`upgrade-openclaw-safely`)

Assess OpenClaw releases, upgrade an installation, or recover a failed update using verified backups, official durable handoff and runtime evidence.

- ⭐ 0 | ⬇ 913

### [概念设计](https://clawhub.ai/agenticweb4/skills/concept-design-cn) (`concept-design-cn`)

定义概念与同步规则，编写规格、实现和审查软件

- ⭐ 0 | ⬇ 21

### [Concept design](https://clawhub.ai/agenticweb4/skills/concept-design) (`concept-design`)

Design software with concepts and synchronization rules

- ⭐ 0 | ⬇ 633

### [RenderMark](https://clawhub.ai/jmsaavedra/skills/rendermark) (`rendermark`)

Professional markdown rendering, export, and publishing via MCP. Use when user asks to "render markdown", "export to PDF", "convert to DOCX", "create a document", "publish a document", "share a link", "make a slide deck", "diff two markdown files", "export to HTML", "create a shareable document", "sync docs from GitHub", or "generate an image of this markdown". Do NOT use for simple markdown editing, code generation, or general writing that doesn't need styled output.

- ⭐ 0 | ⬇ 1458

### [Pet Pica Behavior Recognition | 宠物异食行为识别（啃咬电线/塑料）](https://clawhub.ai/18072937735/skills/smyx-pet-pica-behavior-recognition-analysis) (`smyx-pet-pica-behavior-recognition-analysis`)

Triggers when a user provides an indoor camera video for analysis; supports local uploads or network URLs to call server-side APIs for pet pica-behavior recognition, detecting contact between the pet's mouth and non-food hazardous items (electric wires, plastic bags, socks, tissues, toy fragments, etc.); when the contact lasts ≥ 2 seconds, outputs a warning signal to help prevent intestinal obstruction, electric shock and other dangers (without diagnosing diseases). Application scenarios: indoor cameras, pet safety monitoring, smart-home security. | 当用户提供室内监控视频时，触发本技能进行异食行为识别；支持通过上传本地视频或网络视频URL，调用服务端API检测宠物嘴部与电线、塑料袋、袜子、纸巾、玩具碎片等非食物物品的接触动作；持续接触 ≥ 2 秒时输出预警信号，预防肠梗阻、触电等危险（不诊断疾病）。应用场景：室内摄像头、宠物安全监控、智能家居安防。

- ⭐ 0 | ⬇ 2118

### [GitLab Agent](https://clawhub.ai/xrowgmbh/skills/xrowgmbh-gitlab-agent) (`xrowgmbh-gitlab-agent`)

Operate assigned GitLab work with owner-verified project access and guarded MR delivery.

- ⭐ 1 | ⬇ 7228

### [GitLab Agent Profile](https://clawhub.ai/xrowgmbh/skills/xrowgmbh-gitlab-agent-profile) (`xrowgmbh-gitlab-agent-profile`)

Maintain the GitLab agent profile page and static contribution performance chart.

- ⭐ 0 | ⬇ 6471

### [tld-expert](https://clawhub.ai/bill-makes/skills/tld-expert) (`tld-expert`)

Pick a domain name and ending, check if it can be registered, and find where it is cheapest to register and renew, using tld.expert's free live data (no key). Use when a user is naming a product or business, asks which TLD to use (.com vs .io vs .ai), asks if a domain is available or taken, or asks what a domain costs.

- ⭐ 0 | ⬇ 2

### [GitLab Meeting Assistant](https://clawhub.ai/xrowgmbh/skills/xrowgmbh-gitlab-meeting-assistant) (`xrowgmbh-gitlab-meeting-assistant`)

Capture meeting features and bugs on explicit request

- ⭐ 0 | ⬇ 768

---

## 🏆 本周热门精选 Top10

### [中文公文写作](https://clawhub.ai/gongyu0918-debug/skills/chinese-official-writing) (`chinese-official-writing`)

用于中文公文、事务性材料和新闻稿件的起草、改写、压缩、润色、审校、文种核对、去口语化、降 AI 味及 Word 格式处理，适用于机关、企事业单位、学校和新闻机构。涵盖申请、请示、报告、通知、通告、意见、决定、决议、议案、公报、命令、函、复函、批复、说明、方案、纪要、公告、公示、通报、制度、规定、办法、细则、操作规程、工作要点、总结、调研、讲话、致辞、主持词、述职、可研、审查材料、技术需求、新闻消息、编者按、新闻评论，以及采购、整改、反馈和 AI 算力等场景。

- ⭐ 1 | ⬇ 10961

### [GitLab Agent Self Improvement](https://clawhub.ai/xrowgmbh/skills/xrowgmbh-self-improvement) (`xrowgmbh-self-improvement`)

A skill for personal growth and self-improvement.

- ⭐ 0 | ⬇ 7869

### [GitLab Hackathon](https://clawhub.ai/xrowgmbh/skills/xrowgmbh-gitlab-hackathon) (`xrowgmbh-gitlab-hackathon`)

Plan and execute fair GitLab hackathon participation, including Quarterly and Transcend Hackathons, by analyzing rules, selecting qualifying issues/MRs, tracking scoring levers, and keeping an exploit watchlist.

- ⭐ 0 | ⬇ 7261

### [GitLab Agent](https://clawhub.ai/xrowgmbh/skills/xrowgmbh-gitlab-agent) (`xrowgmbh-gitlab-agent`)

Operate assigned GitLab work with owner-verified project access and guarded MR delivery.

- ⭐ 1 | ⬇ 7228

### [Image Generation](https://clawhub.ai/xrowgmbh/skills/xrowgmbh-image-generation) (`xrowgmbh-image-generation`)

Create or revise document, PDF, web, or review images with the requested format, sharp raster output, and artifact validation.

- ⭐ 1 | ⬇ 7050

### [GitLab Agent Profile](https://clawhub.ai/xrowgmbh/skills/xrowgmbh-gitlab-agent-profile) (`xrowgmbh-gitlab-agent-profile`)

Maintain the GitLab agent profile page and static contribution performance chart.

- ⭐ 0 | ⬇ 6471

### [FDE Skill](https://clawhub.ai/kongfangxun/skills/sofagent) (`sofagent`)

FDE Skill——帮 FDE（前线部署工程师）更好完成企业 AI 落地的方法论 Skill。约束 Agent 行为、审计每次变更、沉淀经验。 底层实现叫约束层——一个层五种能力：注入·审计·回溯·沉淀·进化。FORGE 自迭代工具链是内部开发工具。 内置持续优化模式（sustain），自动读 audit 报告趋势生成优化报告。

- ⭐ 1 | ⬇ 4975

### [CI Tools Pipeline](https://clawhub.ai/xrowgmbh/skills/xrowgmbh-ci-tools-pipeline) (`xrowgmbh-ci-tools-pipeline`)

Build and maintain GitLab CI/CD pipelines with the CI Tools Components Catalog at ci-tools.xrow.de. Use when creating or fixing .gitlab-ci.yml files, choosing CI Tools components, validating component inputs, or designing continuous delivery pipelines for applications, Helm charts, containers, packages, documentation, infrastructure, and GitOps.

- ⭐ 0 | ⬇ 4927

### [rentahuman](https://clawhub.ai/alexanderliteplo/skills/rentahuman) (`rentahuman`)

Hire humans for physical-world tasks via RentAHuman.ai. Search available humans by skill, post bounties, review applications, and coordinate real-world work. Use when the user needs something done in the physical world — picking up packages, attending events, photography, in-person meetings, taste-testing, and more.

- ⭐ 2 | ⬇ 4327

### [aeo](https://clawhub.ai/arberx/skills/aeo) (`aeo`)

Run AEO audits, preview branch audits, changed-page sitemap audits, local/private preview audits with explicit opt-in, sitemap origin rewriting, static-output audits, regression comparisons, site fixes, schema validation, and llms.txt generation.

- ⭐ 1 | ⬇ 4267

---

## 📊 趋势分析

本周 Top 30 标签：

- `image`: 29 次
- `agent`: 25 次
- `client`: 18 次
- `data`: 18 次
- `code`: 17 次
- `video`: 16 次
- `github`: 16 次
- `user`: 15 次
- `asks`: 15 次
- `needs`: 15 次
- `psyb0t`: 15 次
- `kraken`: 14 次
- `already`: 13 次
- `unofficial`: 13 次
- `typed`: 13 次
- `freqtrade`: 13 次
- `through`: 12 次
- `skill`: 12 次
- `generated`: 12 次
- `imports`: 12 次
- `list`: 11 次
- `server`: 11 次
- `package`: 11 次
- `oapi`: 11 次
- `codegen`: 11 次
- `users`: 11 次
- `helps`: 11 次
- `animated`: 10 次
- `hcloud`: 10 次
- `name`: 10 次

---

## 📋 统计摘要

| 指标 | 值 |
|---|---|
| 采集技能总数 | 100 |
| 本周新增 | 27 |
| 本周更新 | 73 |
| 热门精选Top5 | [中文公文写作](https://clawhub.ai/gongyu0918-debug/skills/chinese-official-writing), [GitLab Agent Self Improvement](https://clawhub.ai/xrowgmbh/skills/xrowgmbh-self-improvement), [GitLab Hackathon](https://clawhub.ai/xrowgmbh/skills/xrowgmbh-gitlab-hackathon), [GitLab Agent](https://clawhub.ai/xrowgmbh/skills/xrowgmbh-gitlab-agent), [Image Generation](https://clawhub.ai/xrowgmbh/skills/xrowgmbh-image-generation) |
| 生成时间 | 2026-11-05T08:51:29.686Z |
