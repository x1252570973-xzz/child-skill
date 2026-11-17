# 来源、许可与检索记录

收录日期：2026-11-17。目标：找出**开源**的「健康科普 / 儿童健康科普 / 口播」类 Agent Skill。同日完成两批收录：第一批 17 个技能（健康科普与口播），第二批 30 个技能（儿童健康科普专辑）。

## 一、已收录的上游项目

### 1. LeoYeAI/agent-master-skills

| 项 | 值 |
| --- | --- |
| 仓库 | https://github.com/LeoYeAI/agent-master-skills |
| 默认分支 | `main` |
| Star | 2199 |
| 许可证 | **MIT**（GitHub 已识别，LICENSE 原文见 `LICENSES/LeoYeAI-agent-master-skills-MIT.txt`，Copyright (c) 2026 MyClaw.ai (LeoYeAI)） |
| 技能作者 | AIPOCH（`audio-script-writer` 的 `SKILL.md` frontmatter 中 `skill-author`）；其余技能见各自 frontmatter 的 `submitted_by` |
| 第一批收录 | `skills/audio-script-writer/`（SKILL.md、_meta.json、requirements.txt、scripts/main.py、references/guidelines.md） |
| 第二批收录 | `skills/childcare-essentials/`、`skills/parenting-psychology/`、`skills/family-emergency-planning/` 三个 SKILL.md → `skills/child-health/同名目录/` |

`audio-script-writer`：把医学 / 科研书面内容转成播客、教育视频、有声书、旁白脚本，含口语化改写、医学术语发音指南、时长与语速估算、多格式模板、配音语气提示。后三个是 0–5 岁照护、0–18 岁亲子心理与家庭应急的英文长篇技能包。

### 2. yemugua/agent-skills

| 项 | 值 |
| --- | --- |
| 仓库 | https://github.com/yemugua/agent-skills |
| 默认分支 | `main` |
| Star | 0 |
| 许可证 | 仓库内 `LICENSE` 声明 "MIT License, Copyright (c) 2026"；**GitHub API 返回 `NOASSERTION`**（未被识别为标准 MIT 文本），再分发前建议二次确认 |
| 第一批收录 | `skills/health-popular-science/`、`skills/voiceover-script/` |
| 第一批上游路径 | `app-guides/<slug>/SKILL.md`、`self-media/<slug>/SKILL.md`、`video-creation2/<slug>/SKILL.md`、`health-yanhou-yaoyin-baohu/SKILL.md` |
| 第二批收录 | `skills/child-health/popular-science-templates/`（23 个） |
| 第二批上游路径 | `health/pediatric/<slug>/SKILL.md`、`health/kids/<slug>/SKILL.md`、`parenting/health/<slug>/SKILL.md` |

该仓库是大型中文技能集合（约 2.9 万个 `SKILL.md`），其中带「健康科普」标记的技能有 240 个、与「口播」相关的有 28 个，儿童健康相关目录包括 `baby-care*`、`baby-feed`、`kids-care*`、`kids-health`、`kids-safety*`、`health/pediatric`、`health/kids`、`parenting/health` 等。第一批精选 10 个健康科普 + 6 个口播技能；第二批精选 23 篇**有实质要点与就医红线**的儿科速查。两批均保持原文未改动，目录名保留上游拼音 slug 以便追溯。

第二批刻意**没有**收录大量占位式模板：`app-guides/` 下的通用科普模板（正文是「哪些人建议做、频率如何（参考公开指南）」之类的占位句）、`kids-care2/` 中与标题不符的模板（例如名为「勿酒精擦」但正文讲吼叫与贴标签）、以及仅 200–300 字节的空壳条目。

### 3. runyuan-wang/nutrition-assistants（第二批新增）

| 项 | 值 |
| --- | --- |
| 仓库 | https://github.com/runyuan-wang/nutrition-assistants |
| 默认分支 | `main` |
| Star | 9 |
| 许可证 | **MIT**（GitHub 已识别；根 LICENSE 原文见 `LICENSES/runyuan-nutrition-assistants-MIT.txt`，Copyright (c) 2026 王润圆 Runyuan Wang）。`nutrition-risk-screening-calculator/` 另有独立 MIT LICENSE，已随包收录 |
| 收录路径 | `skills/child-health/<包名>/` |
| 收录包 | `child-obesity-food-guide-skill/`、`child-obesity-tcm-prevention-skill/`（含 `en/`、`ja/`）、`stunting-dietary-guide/`、`nutrition-risk-screening-calculator/` |

依据的公开指南：国家卫生健康委《儿童青少年肥胖食养指南（2024 年版）》、《儿童青少年生长迟缓食养指南（2023 年版）》、中华中医药学会《儿童青少年肥胖治未病干预指南》（2026）、STRONGkids / STAMP 等儿童营养风险筛查量表。为保持技能可用，连同 `knowledge_base.md`、`recipes_data.md`、`system_prompt.md`、`kpk_*.md`、`src/*.py`、`references/scoring.md` 等支撑文件一并收录；仅省略上游安装脚本、测试与二进制示例文件。

## 二、找到但未收录的候选（及原因）

### 第一批

| 候选 | 说明 | 未收录原因 |
| --- | --- | --- |
| `doctor-popular-science`（Med Skill Store） | 中文医生科普文章 + 短视频口播脚本，含合规边界、输入协议、内容路由，内容与需求**最贴合** | 站点为 SPA，未标明开源许可证，也找不到对应 GitHub 仓库 → 不满足「开源」 |
| `health-explainer-video`（SkillHub，`@user_738c00b9/health-explainer-video`） | 「健康科普视频·养生口播」，一分钟科普口播稿 + 分镜 + 标题 + 海报文案 | 社区发布、标记 `requires_api_key=true`，非 GitHub 开源仓库，无许可证 |
| `health-content-writer`（`caishengold/ai-agent-ops`） | 中文健康科普写作，含调研、反幻觉、来源引用、医疗合规（严格级），内容质量很高 | 仓库**无 LICENSE 文件**（GitHub `NOASSERTION`），授权不明 |
| `youtube-script-master` / `youtube-script-hinglish`（`drshailesh88/integrated_content_OS`） | 心脏病学科普 YouTube 脚本，循证 + PubMed + 辟谣结构 | 仓库无 LICENSE；且强依赖私有 research-engine 数据管线，脱离后不可用 |
| `mofyer/pop-science-video` | MIT 开源科普视频生成工具（分镜、配音、成片） | 是完整项目 / 工具，不是 `SKILL.md` 技能包，故只在清单中索引：https://github.com/mofyer/pop-science-video |
| `Alchemica369/local-explainer-video` | 把临床报告转成患者易懂的讲解视频（本地离线） | 无 LICENSE，且是应用不是技能包 |
| `majiayu000/claude-skill-registry` | MIT、742 Star 的大型技能注册表，含 200+ 医疗类技能 | 第一批核实为可靠开源来源，但技能多为医疗信息化 / OCR / 病历方向；第二批复核其 3.3 万个 `SKILL.md` 路径，未发现儿童健康科普类技能 |
| `SpaceZephyr/creator-buddy`、`wwwzhouhui/skills_collection` | 含口播稿 / 科普视频类技能（1917 / 297 Star） | GitHub 均返回 `NOASSERTION`，无明确许可证 |

### 第二批（儿童健康方向）

| 候选 | 说明 | 未收录原因 |
| --- | --- | --- |
| `huifer/wellally-health-skills` | 有 `child-development`、`child-illness`、`child-mental`、`child-nutrition`、`child-safety`、`child-sleep`、`child-vaccine`、`growth`、`puberty` 共 9 个儿童健康技能，每个约 5–7 KB，基于 ASQ-3 / Denver II / WHO 生长曲线，**质量很高、最贴题** | 仓库无 LICENSE（GitHub `NOASSERTION`），README 明写 **"Copyright (c) Wellally. All rights reserved."** → 不是开源，不能收录。注意同作者的 `huifer/WellAlly-health`（MIT、967★）是另一个仓库，并不包含这些儿童技能，不能据此推定授权 |
| `caishengold/ai-agent-ops` 的 `baby-product-reviewer` / `dental-content-writer` / `vision-care-writer` | 婴幼儿用品评测、口腔与视力科普写作 | 仓库仍无 LICENSE（`NOASSERTION`），沿用第一批结论 |
| `runyuan-wang/nutrition-assistants` 的 `nutrition-lesson-generator-zh` | MIT，营养科普课程生成器（讲稿 / 大纲 / PPT + PubMed 引用校验），可做儿童营养科普内容 | 已确认 MIT，但不专属于儿童方向；本批聚焦儿童主题，留作后续扩展。仓库内另有 `china-food-composition` 等通用营养技能同理 |
| `smyx-sunjinhui/smyx-open-claw-skills` | MIT，含 `infant-cry-analysis`、`infant-suffocation-warning-analysis`、`infant-safety-monitoring-analysis`、`child-dangerous-behavior-recognition-analysis`、`autism-analysis` 等 | 属摄像头 / 视觉信号监测分析技能，依赖外部 API 与图像输入，不是科普内容技能 |
| `sickn33/agentic-awesome-skills` | MIT、约 4.9 万 Star、9500+ 技能 | 按 `child / pediatric / infant` 检索未发现儿科健康类 SKILL.md |
| `Ruacha00/MediPet`、`Zh-Med/Skill-of-Diagnostic`、`Biangi/medical-consultation-prep`、`lyjps/Capybara` | 医疗问诊 / 诊断辅助类技能 | 无明确许可证或为通用诊疗方向，非儿童科普 |

如果后续确认了上述某个项目的授权（尤其是 `wellally-health-skills`），可以按同样的目录结构补录，并在本文件登记。

## 三、检索方式

- GitHub 代码搜索：`"健康科普" filename:SKILL.md`、`"口播" filename:SKILL.md`、`"口播稿" filename:SKILL.md`、`"儿童" filename:SKILL.md`、`"儿科" filename:SKILL.md`、`"儿童" "健康科普" filename:SKILL.md`、`child OR pediatric OR infant filename:SKILL.md repo:<owner>/<repo>` 等。
- GitHub `git/trees/<branch>?recursive=1` 拉取大仓库完整路径清单，按拼音 / 英文关键词（ertong、xiaoer、yinger、yimiao、shouzukou、haimulike、pediatric、child-obesity、STRONGkids 等）分组筛选，再逐个读取内容判断质量。
- GitHub 仓库元数据 API 核对 `license.spdx_id`、star、默认分支；**逐仓库读取 LICENSE 原文与 README 的 License 段**，不依赖第三方目录站的标注（本次正是靠这一步排除了 `wellally-health-skills`）。
- 公开技能目录（SkillHub、Med Skill Store、Skillselion、VibeCrowd）交叉比对技能名称与来源仓库。

## 四、归属与再分发

所有收录文件均**未修改**，保留原 `SKILL.md` frontmatter（含 `name`、`description`、`license`、`metadata.skill-author` / `submitted_by`）。MIT 许可证要求保留版权声明与许可文本，因此三份上游 LICENSE 原文均放在 `LICENSES/`，各专辑目录下另有 `SOURCE.md` 记录具体来源路径与链接。

`yemugua/agent-skills` 的授权状态需在再分发前二次确认：其 LICENSE 只有一行 MIT 声明，GitHub 返回 `NOASSERTION`。本仓库已在 README、`_INDEX.md`、`SOURCE.md` 三处明确标注该风险。
