# 来源与许可（自动剪辑专辑）

收录日期：2026-11-17。本专辑 16 个技能全部**原样复制自上游**，未修改任何内容；仅按来源重新组织目录。10 个来源的 LICENSE 原文统一放在 [`../../LICENSES/`](../../LICENSES/)，部分技能包内另有独立的 LICENSE 文件，随包保留。

| # | 上游仓库 | 分支 | Star | 许可证 | 本仓库收录路径 | 上游原始路径 | LICENSE 副本 |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | [kajisho5/ffmpeg-skill](https://github.com/kajisho5/ffmpeg-skill) | `main` | 7590 | **MIT** | `ffmpeg-skill/` | `SKILL.md`、`skills/ffmpeg-skill/SKILL.md`、`scripts/*.py`（42 工具）、`mcp/server.py` | `LICENSES/kajisho5-ffmpeg-skill-MIT.txt` |
| 2 | [op7418/Youtube-clipper-skill](https://github.com/op7418/Youtube-clipper-skill) | `main` | 2330 | **MIT** | `youtube-clipper/` | `SKILL.md`、`scripts/`、`references/`、`templates/`、`README.zh-CN.md`、`.env.example` | `LICENSES/op7418-Youtube-clipper-skill-MIT.txt` |
| 3 | [Backtthefuture/videocut-skills](https://github.com/Backtthefuture/videocut-skills) | `main` | 13 | **MIT** | `videocut-skills/剪口播/`、`videocut-skills/docs/` | `剪口播/`（SKILL.md + 9 个 scripts + 用户习惯/）、`docs/API_KEY_SETUP.md` | `LICENSES/Backtthefuture-videocut-skills-MIT.txt` |
| 4 | [xianyu110/ecommerce-video-skills](https://github.com/xianyu110/ecommerce-video-skills) | `main` | 144 | **MIT** | `ecommerce-video-skills/{ffmpeg-auto-assemble,live-stream-clips,platform-spec-export}/` | `skills/<同名>/`（SKILL.md + scripts/） | `LICENSES/xianyu110-ecommerce-video-skills-MIT.txt` |
| 5 | [zenstory-ai/video-recap-skills](https://github.com/zenstory-ai/video-recap-skills) | `main` | 635 | **MIT** | `video-recap/` | `skills/video-recap/`（SKILL.md、references/、scripts/、assets/dashboard/） | `LICENSES/zenstory-video-recap-skills-MIT.txt` |
| 6 | [ZJU-REAL/Easel](https://github.com/ZJU-REAL/Easel) | `main` | 4743 | **Apache-2.0** | `easel-video-skills/{auto-short-video,clipify,video-editing}/` | `skills/builtin/<同名>/`（SKILL.md、EASEL-META.md、scripts/） | `LICENSES/ZJU-REAL-Easel-Apache-2.0.txt` |
| 7 | [bytedance/agentkit-samples](https://github.com/bytedance/agentkit-samples) | `main` | 492 | **Apache-2.0** | `byted-mediakit/{byted-mediakit-videoedit,byted-mediakit-process-tools}/` | `skills/<同名>/`（SKILL.md、references/、scripts/、template/、各自 LICENSE） | `LICENSES/bytedance-agentkit-samples-Apache-2.0.txt` |
| 8 | [sun-guannan/VectCutAPI](https://github.com/sun-guannan/VectCutAPI) | `main` | 2383 | **Apache-2.0** | `vectcut/skill/`、`vectcut/capcut-director/` | `vectcut-skill/skill/`（SKILL.md、references/、scripts/）、`.agents/skills/capcut-director/SKILL.md` | `LICENSES/sun-guannan-VectCutAPI-Apache-2.0.txt`（包内另有 `vectcut/LICENSE`） |
| 9 | [znyupup/ai-video-editing-skill](https://github.com/znyupup/ai-video-editing-skill) | `main` | 183 | **MIT** | `vlog-auto-edit/` | `SKILL.md`、`README.md`、`examples/`、`scripts/`、`templates/` | `LICENSES/znyupup-ai-video-editing-skill-MIT.txt` |
| 10 | [foryourhealth111-pixel/Vibe-Skills](https://github.com/foryourhealth111-pixel/Vibe-Skills) | `main` | 3827 | **Apache-2.0** | `video-studio/` | `bundled/skills/video-studio/`（SKILL.md、references/、scripts/） | `LICENSES/Vibe-Skills-Apache-2.0.txt` |

## 检索与筛选

- GitHub 代码搜索：`"自动剪辑" filename:SKILL.md`、`"视频剪辑" filename:SKILL.md`、`video-edit OR ffmpeg filename:SKILL.md` 等；公开技能目录站交叉比对。
- `git/trees/main?recursive=1` 拉取候选仓库完整文件清单，按**是否带 scripts / references / CLI** 过滤，只保留完整技能包；再逐个读 SKILL.md frontmatter 确认触发条件与依赖。
- GitHub 仓库元数据 API 核对 `license.spdx_id`、star、默认分支；逐个读取根 LICENSE 原文（10 份均为标准 MIT 或 Apache License 2.0 文本）。
- 下载后扫描是否含疑似硬编码密钥（`sk-`、`AKIA`、`ghp_` 等），结果为空；`.env.example` 仅为占位模板。

## 找到但未收录（第三批）

| 候选 | 未收录原因 |
| --- | --- |
| `sun-guannan/VectCutSkill`（16★）、`Hommy-master/capcut-mate-skill`（60★）、`JustAIPlay/auto_edit_video`、`Gonglitian/agent-skills` | GitHub 均返回 `NOASSERTION`，无明确许可证。其中 VectCutSkill 的剪映能力已由**同作者的 Apache-2.0 仓库** `VectCutAPI` 覆盖，故收录后者 |
| `wubin1836/ai-hive-agent-skills`（MIT，含 `talking-video-silence-cut-ai-hive`、`video-editing-toolkit-ai-hive` 等） | 仓库含 6000+ SKILL.md 且多为纯提示词模板，本批聚焦可运行技能包；留作后续扩展 |
| `modbender/skill-library-mcp`（MIT，`autoclip-pro`、`video-pipeline-bundle`） | 第三方再打包的技能库，无法确认上游授权链 |
| `sickn33/agentic-awesome-skills`（MIT、约 4.9 万★）、`LeoYeAI/agent-master-skills`（MIT）、`majiayu000/claude-skill-registry`（MIT、744★） | 已核实为可靠开源来源，但按 `video-edit / ffmpeg / 剪辑` 定向检索未发现专门的自动剪辑技能（`LeoYeAI` 的 `fcpx-assistant`、`tencent-mps` 属剪辑辅助 / 云媒体处理，非自动剪辑工作流） |
| `yikart/AiToEarn`（MIT、2.8 万★）的 `editing-videos` | 与该项目后端强绑定，脱离后不可用 |
| `mofyer/pop-science-video`（MIT） | 是完整应用而非 `SKILL.md` 技能包（第一批已登记） |
| `ops120/video-recap-skills-plus`、`ceoifung/ai-short-drama`、`lj1270998580-crypto/JaygoCut`、`Wanfeng1028/muse` | 与已收录的 `video-recap` / `ffmpeg-auto-assemble` / 剪映自动化能力重复，或为二次打包，未重复收录 |

## 归属与再分发

MIT 与 Apache-2.0 均要求保留版权与许可声明：10 份根 LICENSE 原文放在 `LICENSES/`，`byted-mediakit/*/LICENSE`、`vectcut/LICENSE`、`video-recap/references/jianying/LICENSE.duo-video` 等包内许可证随原路径保留，所有 `SKILL.md` 的 frontmatter（含 `name`、`description`、`version`、`author`、`allowed-tools`）未改动。Apache-2.0 仓库如做修改，需按许可证第 4 条注明变更；本仓库未作修改。若上游更新，请对照上表原始路径重新同步。
