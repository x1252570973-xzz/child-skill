# 来源、许可与检索记录

收录日期：2026-11-17。目标：找出**开源**的「健康科普 / 口播」类 Agent Skill。

## 一、已收录的上游项目

### 1. LeoYeAI/agent-master-skills

| 项 | 值 |
| --- | --- |
| 仓库 | https://github.com/LeoYeAI/agent-master-skills |
| 默认分支 | `main` |
| Star | 2199 |
| 许可证 | **MIT**（GitHub 已识别，LICENSE 原文见 `LICENSES/LeoYeAI-agent-master-skills-MIT.txt`，Copyright (c) 2026 MyClaw.ai (LeoYeAI)） |
| 技能作者 | AIPOCH（`SKILL.md` frontmatter 中 `skill-author`） |
| 收录路径 | `skills/audio-script-writer/` |
| 上游原始路径 | `skills/audio-script-writer/`（SKILL.md、_meta.json、requirements.txt、scripts/main.py、references/guidelines.md） |

`audio-script-writer`：把医学 / 科研书面内容转成播客、教育视频、有声书、旁白脚本，含口语化改写、医学术语发音指南、时长与语速估算、多格式模板、配音语气提示。

### 2. yemugua/agent-skills

| 项 | 值 |
| --- | --- |
| 仓库 | https://github.com/yemugua/agent-skills |
| 默认分支 | `main` |
| Star | 0 |
| 许可证 | 仓库内 `LICENSE` 声明 "MIT License, Copyright (c) 2026"；**GitHub API 返回 `NOASSERTION`**（未被识别为标准 MIT 文本），再分发前建议二次确认 |
| 收录路径 | `skills/health-popular-science/`、`skills/voiceover-script/` |
| 上游原始路径 | `app-guides/<slug>/SKILL.md`、`self-media/<slug>/SKILL.md`、`video-creation2/<slug>/SKILL.md`、`health-yanhou-yaoyin-baohu/SKILL.md` |

该仓库是大型中文技能集合，其中带「健康科普」标记的技能有 240 个、与「口播」相关的有 28 个。本仓库精选了 10 个健康科普 + 6 个口播相关技能，均为轻量模板型指南。目录名保留上游拼音 slug 以便追溯。

## 二、找到但未收录的候选（及原因）

| 候选 | 说明 | 未收录原因 |
| --- | --- | --- |
| `doctor-popular-science`（Med Skill Store） | 中文医生科普文章 + 短视频口播脚本，含合规边界、输入协议、内容路由，内容与需求**最贴合** | 站点为 SPA，未标明开源许可证，也找不到对应 GitHub 仓库 → 不满足「开源」 |
| `health-explainer-video`（SkillHub，`@user_738c00b9/health-explainer-video`） | 「健康科普视频·养生口播」，一分钟科普口播稿 + 分镜 + 标题 + 海报文案 | 社区发布、标记 `requires_api_key=true`，非 GitHub 开源仓库，无许可证 |
| `health-content-writer`（`caishengold/ai-agent-ops`） | 中文健康科普写作，含调研、反幻觉、来源引用、医疗合规（严格级），内容质量很高 | 仓库**无 LICENSE 文件**（GitHub `NOASSERTION`），授权不明 |
| `youtube-script-master` / `youtube-script-hinglish`（`drshailesh88/integrated_content_OS`） | 心脏病学科普 YouTube 脚本，循证 + PubMed + 辟谣结构 | 仓库无 LICENSE；且强依赖私有 research-engine 数据管线，脱离后不可用 |
| `mofyer/pop-science-video` | MIT 开源科普视频生成工具（分镜、配音、成片） | 是完整项目 / 工具，不是 `SKILL.md` 技能包，故只在清单中索引：https://github.com/mofyer/pop-science-video |
| `Alchemica369/local-explainer-video` | 把临床报告转成患者易懂的讲解视频（本地离线） | 无 LICENSE，且是应用不是技能包 |
| `majiayu000/claude-skill-registry` | MIT、742 Star 的大型技能注册表，含 200+ 医疗类技能 | 已核实为可靠开源来源，但技能多为医疗信息化 / OCR / 病历方向，与「科普口播」不直接对口；留作后续扩展：https://github.com/majiayu000/claude-skill-registry |
| `SpaceZephyr/creator-buddy`、`wwwzhouhui/skills_collection` | 含口播稿 / 科普视频类技能（1917 / 297 Star） | GitHub 均返回 `NOASSERTION`，无明确许可证 |

如果后续确认了上述某个项目的授权，可以按同样的目录结构补录，并在本文件登记。

## 三、检索方式

- GitHub 代码搜索：`"健康科普" filename:SKILL.md`、`"口播" filename:SKILL.md`、`"口播稿" filename:SKILL.md`、`"健康科普" "口播" filename:SKILL.md`、`repo:` 定向检索等。
- GitHub 仓库元数据 API 核对 `license.spdx_id`、star、默认分支。
- 公开技能目录（SkillHub、Med Skill Store、Skillselion、VibeCrowd）交叉比对技能名称与来源仓库。
- 逐仓库读取 `LICENSE` 原文确认授权，不依赖第三方目录站的标注。

## 四、归属与再分发

所有收录文件均**未修改**，保留原 `SKILL.md` frontmatter（含 `name`、`description`、`license`、`metadata.skill-author`）。MIT 许可证要求保留版权声明与许可文本，因此上游 LICENSE 原文一并放在 `LICENSES/`，各技能目录下另有 `SOURCE.md` 记录具体来源路径与链接。
