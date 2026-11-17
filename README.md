# child-skill · 健康科普、口播与自动剪辑 Agent Skills 收录库

从 GitHub 上**明确开源**的项目中，挑选「健康科普」「儿童健康科普」「口播 / 配音脚本」与「自动剪辑」相关的 Agent Skill（`SKILL.md` 格式），原样收录并保留每个来源的作者、许可证和原始链接。

> 本仓库只做收录与索引，不修改上游技能内容。原创作者与版权归各自上游项目所有。

## 收录概览

| 目录 | 内容 | 数量 | 上游仓库 | 许可证 |
| --- | --- | --- | --- | --- |
| `skills/audio-script-writer/` | 医学 / 健康内容转口播、播客、配音脚本（含 CLI 脚本与参考文件） | 1 个完整技能包 | [LeoYeAI/agent-master-skills](https://github.com/LeoYeAI/agent-master-skills) | MIT |
| `skills/health-popular-science/` | 中文健康科普：癌症筛查、血脂管理、体检准备、报告解读等 | 10 个 | [yemugua/agent-skills](https://github.com/yemugua/agent-skills) | MIT（仓库内 LICENSE 声明） |
| `skills/voiceover-script/` | 中文口播稿与口播实务：钩子、结构、口语化、提词、语速、嗓音保护 | 6 个 | [yemugua/agent-skills](https://github.com/yemugua/agent-skills) | MIT（仓库内 LICENSE 声明） |
| `skills/child-health/` | **儿童健康科普专辑**：婴幼儿照护、亲子心理、儿童肥胖 / 生长迟缓食养、营养风险筛查、中文儿科速查 | **30 个技能 / 75 个上游文件** | LeoYeAI、[runyuan-wang/nutrition-assistants](https://github.com/runyuan-wang/nutrition-assistants)、yemugua | MIT ×2 + MIT 声明（`NOASSERTION`）×1 |
| `skills/auto-video-editing/` | **自动剪辑专辑**：本地 FFmpeg 工具链、长视频智能切片、口播自动剪、一键成片、剪映自动化、平台规格导出 | **16 个技能 / 301 个上游文件** | 10 个仓库 | MIT ×6、Apache-2.0 ×4 |
| `LICENSES/` | 上游许可证原文 | 13 份 | — | — |

合计 **63 个技能、421 个文件（约 5.3 MB）**。完整的来源、许可与「找到但未收录」的候选清单见 [SOURCES.md](SOURCES.md)；各专辑清单见 [`skills/child-health/_INDEX.md`](skills/child-health/_INDEX.md) 与 [`skills/auto-video-editing/_INDEX.md`](skills/auto-video-editing/_INDEX.md)。

## 目录结构

```
child-skill/
├── README.md
├── SOURCES.md
├── LICENSES/                     # 13 份上游许可证原文
│   ├── LeoYeAI-agent-master-skills-MIT.txt
│   ├── yemugua-agent-skills-MIT.txt
│   ├── runyuan-nutrition-assistants-MIT.txt
│   ├── kajisho5-ffmpeg-skill-MIT.txt
│   ├── ...（其余 9 份，见 SOURCES.md）
└── skills/
    ├── audio-script-writer/          # 医学内容 → 口播 / 配音脚本（英文，完整包）
    │   └── SKILL.md + _meta.json + scripts/ + references/ + SOURCE.md
    ├── health-popular-science/       # 中文健康科普（10 个）
    ├── voiceover-script/             # 中文口播稿（6 个）
    ├── child-health/                 # 儿童健康科普专辑（30 个）
    │   ├── _INDEX.md / SOURCE.md
    │   ├── childcare-essentials/、parenting-psychology/、family-emergency-planning/
    │   ├── child-obesity-food-guide-skill/、child-obesity-tcm-prevention-skill/
    │   ├── stunting-dietary-guide/、nutrition-risk-screening-calculator/
    │   └── popular-science-templates/（中文儿科速查 23 个）
    └── auto-video-editing/           # 自动剪辑专辑（16 个）
        ├── _INDEX.md / SOURCE.md
        ├── ffmpeg-skill/             # 本地 FFmpeg 42 工具 + MCP（MIT，7590★）
        ├── youtube-clipper/          # YouTube 智能切片 + 双语字幕（MIT）
        ├── videocut-skills/剪口播/   # 口播自动剪（MIT）
        ├── ecommerce-video-skills/   # 一键成片 / 直播切片 / 平台导出（3 个）
        ├── video-recap/              # 视频解说自动成片（MIT）
        ├── easel-video-skills/       # 自动短视频 / clipify / 剪辑编排（Apache-2.0）
        ├── byted-mediakit/           # AI 智能剪辑 + 媒体处理（Apache-2.0）
        ├── vectcut/                  # 剪映 / CapCut 时间线自动化（Apache-2.0）
        ├── vlog-auto-edit/           # Vlog 全自动剪辑工作流（MIT）
        └── video-studio/             # 端到端自动剪辑与抛光（Apache-2.0）
```

## 收录清单

### 一、医学 / 健康内容 → 口播脚本

**`audio-script-writer`** — 把论文、报告、患者教育材料改写成适合「听」的口播稿：句子口语化、医学术语注音、时长与语速估算、播客 / 视频 / 讲义 / 有声书多格式模板、配音语气提示。附带可运行的 `scripts/main.py`（纯标准库，Python 3.7+）。

```bash
python skills/audio-script-writer/scripts/main.py --input article.txt --duration 5 --output script.json
```

### 二、中文健康科普（10 个）

| Skill | 主题 |
| --- | --- |
| `ganaishaicha-yigan-tianbao` | 肝癌筛查（乙肝） |
| `feiaishaicha-gaowei-tianbao` | 肺癌筛查（高危人群） |
| `xuezhiguanli-fucha-tianbao` | 血脂管理（复查） |
| `ruxianaishaicha-muba-tianbao` | 乳腺癌筛查（钼靶） |
| `hpvyutctshaicha-pinlv-tianbao` | HPV 与 TCT 筛查（频率） |
| `zhifanggannizhuan-jiejiu-tianbao` | 脂肪肝逆转（戒酒） |
| `tijianqianzhunbei-kongfu-tianbao` | 体检前准备（空腹） |
| `weichangjingjiancha-zhunbei-tianbao` | 胃肠镜检查（准备） |
| `xuechangguijiedu-sandaxiang-tianbao` | 血常规解读（三大项） |
| `feijiejiesuifang-ct-tianbao` | 肺结节随访（CT） |

### 三、中文口播稿（6 个）

| Skill | 主题 |
| --- | --- |
| `koubogao-gouzi` | 口播稿·开头钩子 |
| `koubogao-jiegou` | 口播稿·结构 |
| `koubogao-kouyuhua` | 口播稿·口语化 |
| `koubo-tici` | 口播·提词 |
| `koubo-yusu` | 口播·语速 |
| `yanhou-sangyin-baohu` | 咽喉与嗓音保护 |

### 四、儿童健康科普专辑（30 个）

| 分组 | 数量 | 内容 | 来源 / 许可 |
| --- | --- | --- | --- |
| 完整照护与心理指南 | 3 | 0–5 岁婴幼儿照护、0–18 岁情绪发育与管教、家庭应急预案（英文长篇，每个约 2.1–2.6 万字符） | LeoYeAI/agent-master-skills · MIT |
| 循证儿童营养与筛查 | 4 | 儿童肥胖食养（2024 国家指南）、肥胖治未病（2026 学会指南，含英/日版）、生长迟缓食养（2023 国家指南）、营养风险筛查计算器（STRONGkids 等，可运行 CLI） | runyuan-wang/nutrition-assistants · MIT |
| 中文儿科速查 | 23 | 发热 / 热性惊厥 / 咳嗽 / 腹泻 / 湿疹 / 近视防控 / 身高体重 / 睡眠 / 挑食 / 说话晚 / 心理情绪 / 体检筛查 / 退烧用药 / 疱疹性咽峡炎等，均含「就医红线」 | yemugua/agent-skills · MIT 声明（`NOASSERTION`） |

完整表格见 [`skills/child-health/_INDEX.md`](skills/child-health/_INDEX.md)。

### 五、自动剪辑专辑（16 个）

| 分组 | 数量 | 代表技能 | 上游 / 许可 |
| --- | --- | --- | --- |
| 本地 FFmpeg 工具链 | 1 | `ffmpeg-skill`：42 个带 `--dry-run` / `--json` 的可校验工具 + MCP server，纯本地无 API Key | [kajisho5/ffmpeg-skill](https://github.com/kajisho5/ffmpeg-skill) · MIT（7590★） |
| 长视频智能切片 | 3 | `youtube-clipper`、`clipify`、`byted-mediakit-videoedit` | op7418、ZJU-REAL、bytedance · MIT / Apache-2.0 |
| 口播自动剪 | 1 | `剪口播`：转录 → 语气词/静音/重复识别 → 审查稿 → 按清单剪辑 | Backtthefuture · MIT |
| 一键成片 / 批量导出 | 4 | `ffmpeg-auto-assemble`、`live-stream-clips`、`platform-spec-export`、`auto-short-video` | xianyu110、ZJU-REAL · MIT / Apache-2.0 |
| 解说 / Vlog 自动成片 | 2 | `video-recap`、`vlog-auto-edit` | zenstory-ai、znyupup · MIT |
| 剪映 / CapCut 自动化 | 2 | `vectcut-api`、`capcut-director` | sun-guannan · Apache-2.0 |
| 媒体处理与端到端编排 | 3 | `byted-mediakit-process-tools`、`video-editing`、`video-studio` | bytedance、ZJU-REAL、Vibe-Skills · Apache-2.0 |

**完整索引（含每个技能的依赖、能力、快速选择表）见 [`skills/auto-video-editing/_INDEX.md`](skills/auto-video-editing/_INDEX.md)**。收录时按「能真正跑起来」筛选：只收带脚本 / CLI / 参考文档的完整技能包，纯提示词占位模板不收。

## 安装使用

这些是标准 `SKILL.md` 格式的 Agent Skill，把单个技能目录复制到你所用 Agent 的 skills 目录即可，例如：

```bash
# Claude Code
cp -r skills/audio-script-writer ~/.claude/skills/

# 儿童健康科普（完整包）
cp -r skills/child-health/child-obesity-food-guide-skill ~/.claude/skills/

# 自动剪辑（注意：ffmpeg-skill 要保持整包目录结构，脚本在 ../../scripts/）
cp -r skills/auto-video-editing/ffmpeg-skill ~/.claude/skills/

# 或项目级，单个中文速查模板
cp -r skills/child-health/popular-science-templates/ertong-fashao .claude/skills/
```

支持 `SKILL.md` 格式的其他 Agent（WorkBuddy、Codex、Cursor 等）同理，放到各自的技能发现目录后重启即可自动加载。带支撑文件（知识库、食谱、Python CLI、FFmpeg 脚本）的完整包请**整个目录**复制，不要只拷 `SKILL.md`。自动剪辑技能另需本机 `ffmpeg`（部分还需 Python 依赖或云服务凭证），详见各技能 README 与 `_INDEX.md` 的「依赖与适用边界」。

## 一条完整的内容流水线

```
voiceover-script/（口播稿结构）→ health-popular-science/ 或 child-health/（科普事实底座）
→ audio-script-writer/（转成可听的口播稿）→ auto-video-editing/（自动剪辑成片）
```

剪口播、去静音、字幕烧录、9:16 平台导出这几步在自动剪辑专辑里都有对应技能。

## 内容质量说明

- `audio-script-writer` 是完整、可直接运行的技能包（约 16 KB 技能文档 + 9 KB CLI 脚本）。
- 儿童专辑里的 3 个英文长篇 + 4 个循证营养包是**信息密度最高**的一组：依据公开发布的国家 / 学会指南，附带知识库、食谱数据、系统提示词与可运行代码，适合做科普长文、家长问答或口播稿的事实底座。
- 自动剪辑专辑是本仓库**工程化程度最高**的一组：10 个来源均经 GitHub API 与 LICENSE 原文双重核对，301 个上游文件里包含 42 个 FFmpeg 工具脚本、剪映 API 客户端、Remotion 模板、字幕与响度处理脚本等。其中 `ffmpeg-skill`、`ecommerce-video-skills/*`、`video-studio`、`vlog-auto-edit` 完全本地运行、不需要 API Key；其余需要 ASR/TTS、火山引擎 mediakit 或 VectCutAPI 云端服务，已在 `_INDEX.md` 逐项标注。
- `yemugua/agent-skills` 中的中文技能是**轻量模板型指南**（每个约 200–1400 字节），给的是结构框架、要点、常见误区与免责红线，适合作为写作骨架或速查卡，不是长篇领域知识库。收录时保持原文未改动；上游存在少量 slug 与主题不符、Markdown 加粗嵌套破损、主题重复等问题，已在 `_INDEX.md` 中如实标注。
- 13 份上游许可证原文已放在 `LICENSES/`。其中 `yemugua/agent-skills` 的 LICENSE 文件仅写了 "MIT License / Copyright (c) 2026"，GitHub 未自动识别为标准 MIT（`NOASSERTION`），再分发时建议二次确认授权。

## 医疗免责声明

本仓库中的健康科普内容**仅供科普与教育目的，不构成医疗建议、诊断或治疗方案**。具体检查、报告解读与用药请以接诊医生为准，不要自行用药或停药。上游技能中已包含相应的合规与免责提醒，使用时请一并保留。自动剪辑专辑是视频处理工具，与健康内容无关，不受本声明约束。

**儿童内容额外提示**：儿童不是成人的缩小版，用药剂量需按体重计算并遵医嘱；3 月龄以下婴儿发热、热性惊厥、呼吸急促或费力、皮疹压不褪色、精神萎靡拒食脱水等情形应立即就医。不要依据科普内容自行给孩子用退烧药、抗生素、驱蚊剂或补充剂，也不要用「视力康复」「按摩降度数」等非循证手段替代正规诊疗。

## 维护

- 收录日期：2026-11-17。第一批 17 个技能（健康科普与口播）；同日第二批增补儿童健康科普 30 个技能；第三批增补自动剪辑 16 个技能。
- 收录原则：上游项目公开可访问、有明确开源许可声明、内容直接相关；不修改原文，保留归属。许可不明或声明「保留所有权利」的项目一律不收录，只登记在 `SOURCES.md` 中。技能包优先收录可运行的完整包而非占位模板。
- 若上游更新，请对照 `SOURCES.md` 中的原始路径重新同步。
