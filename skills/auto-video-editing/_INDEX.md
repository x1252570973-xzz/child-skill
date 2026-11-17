# 自动剪辑技能索引

本次新增 **16 个技能 / 17 份 SKILL.md / 301 个上游文件**（另含 10 份上游许可证与 2 份索引文档，合计 313 个新文件），来自 10 个明确开源的仓库（MIT ×6、Apache-2.0 ×4）。所有文件**原样收录、未修改**，归属与许可证见 [SOURCE.md](SOURCE.md)，全库说明见 [../../README.md](../../README.md)。

收录标准不是「名字里有剪辑」，而是**能真正跑起来**：优先选带脚本、CLI、知识库/参考文档的完整技能包，并逐个核对 `license.spdx_id` 与 LICENSE 原文。纯提示词占位模板一律不收。

## 快速选择

| 你的需求 | 推荐 |
| --- | --- |
| 不想接任何云服务、素材不能外传 | `ffmpeg-skill/`、`ecommerce-video-skills/*`、`video-studio/`、`vlog-auto-edit/`（其中 ffmpeg-skill 与 ffmpeg-auto-assemble 最完整） |
| 长视频自动切高光 / 智能切片 | `youtube-clipper/`、`easel-video-skills/clipify/`、`byted-mediakit/byted-mediakit-videoedit/` |
| 口播视频去口误、去静音、去重复 | `videocut-skills/剪口播/`（与本仓库的口播稿技能正好配套） |
| 从文案 / storyboard 一键生成成片 | `ecommerce-video-skills/ffmpeg-auto-assemble/`、`easel-video-skills/auto-short-video/`、`video-recap/` |
| 剪映 / CapCut 时间线自动化 | `vectcut/skill/`、`vectcut/capcut-director/` |
| 平台规格批量导出 / 交付校验 | `ecommerce-video-skills/platform-spec-export/`、`ffmpeg-skill/` 的 export / check 工具 |

## 完整清单

| 目录 | 技能 | 能力 | 运行依赖 | 来源 / 许可 |
| --- | --- | --- | --- | --- |
| `ffmpeg-skill/` | `ffmpeg-skill` | 本地 FFmpeg 42 工具：裁切/拼接/去静音/重构图/字幕/响度/HDR→SDR/多平台导出与校验；每个工具带 `--dry-run`、`--json` 与机器可读 contract，另含 MCP server | FFmpeg 6.1+ / Python 3.10+，纯标准库，**无需 API Key** | kajisho5/ffmpeg-skill · MIT |
| `youtube-clipper/` | `youtube-clipper` | YouTube 长视频智能切片：下载视频与字幕 → 生成细粒度章节 → 按选择自动剪辑 → 字幕翻译为中英双语并烧录 → 生成总结文案 | yt-dlp、ffmpeg、翻译用 LLM | op7418/Youtube-clipper-skill · MIT |
| `videocut-skills/剪口播/` | `videocut:剪口播` | 口播视频自动剪：转录 → 语气词/静音/重复/残句识别 → 生成审查稿与删除清单 → 按清单剪辑 → 剪后重转录与 AI 字幕校对 | ffmpeg、火山引擎 ASR（需 Key）、Node.js | Backtthefuture/videocut-skills · MIT |
| `ecommerce-video-skills/ffmpeg-auto-assemble/` | `ffmpeg-auto-assemble` | `storyboard.json` → 配音(edge-tts) → Ken Burns/裁切 → xfade 转场 → ASS 字幕花字 → BGM 自动闪避 → 两遍 loudnorm → 9:16 MP4 + SRT | ffmpeg、edge-tts、Pillow，**纯本地** | xianyu110/ecommerce-video-skills · MIT |
| `ecommerce-video-skills/live-stream-clips/` | `live-stream-clips` | 直播录像自动切高光片段 | ffmpeg | xianyu110/ecommerce-video-skills · MIT |
| `ecommerce-video-skills/platform-spec-export/` | `platform-spec-export` | 按平台规格批量导出（分辨率 / 码率 / 时长上限 / 安全区） | ffmpeg | xianyu110/ecommerce-video-skills · MIT |
| `video-recap/` | `video-recap` | 视频解说 / 原声剧情短片自动成片：视频理解 → 导演立意与选镜剪辑 → 解说撰稿校验 → TTS 配音 → 音画混音与字幕渲染；`scripts/recap.py` 可串联全流程 | ffmpeg、可配置 ASR / TTS | zenstory-ai/video-recap-skills · MIT |
| `easel-video-skills/auto-short-video/` | `auto-short-video` | 一句话主题 → 成品短视频：文案 → 配图/AI 视频 → 配音 → 字幕 → BGM → `scripts/assemble.py` 合成 | Easel 制作层零件 + AI 服务 | ZJU-REAL/Easel · Apache-2.0 |
| `easel-video-skills/clipify/` | `clipify` | 智能切片 / 高光提取，含镜头分析、ASS 字幕与运镜脚本 | ffmpeg + 自带分析脚本 | ZJU-REAL/Easel · Apache-2.0 |
| `easel-video-skills/video-editing/` | `video-editing` | 通用视频剪辑编排（Easel 制作层） | Easel 环境 | ZJU-REAL/Easel · Apache-2.0 |
| `byted-mediakit/byted-mediakit-videoedit/` | `byted-mediakit-videoedit` | AI 智能剪辑：结合弹幕/字幕理解视频上下文，按指令抽取高光、拼接加转场、FFmpeg 合成；附 Remotion 动效模板 | 火山引擎 mediakit（部分能力有本地 ffmpeg 回退） | bytedance/agentkit-samples · Apache-2.0 |
| `byted-mediakit/byted-mediakit-process-tools/` | `byted-mediakit-process-tools` | 媒体处理工具集：拼接 / 裁剪 / 增强 / 提取音频 / 音画合成 / 图生视频 / 内容理解，含 `local_ffmpeg_tool.py` 本地回退 | 同上 | bytedance/agentkit-samples · Apache-2.0 |
| `vectcut/skill/` | `vectcut-api` | 剪映 / CapCut 草稿工程编程化：素材、字幕、特效、转场、关键帧、批量处理、AI 生成，支持 HTTP REST + MCP | VectCutAPI 云端服务（需自行部署或申请） | sun-guannan/VectCutAPI · Apache-2.0 |
| `vectcut/capcut-director/` | `capcut-director` | 面向剪映的导演式编排技能 | 同上 | sun-guannan/VectCutAPI · Apache-2.0 |
| `vlog-auto-edit/` | `vlog-auto-edit` | 旅行 Vlog 全自动剪辑完整工作流：素材整理 → 语音转写 → 分镜 / 剪辑计划 → 成片 → 可视化仪表盘；系统级只需 ffmpeg | ffmpeg、Python venv、whisper / funasr | znyupup/ai-video-editing-skill · MIT |
| `video-studio/` | `video-studio` | 端到端「素材 + 文案 + 编排 → 可发布成片」：自动剪 / jumpcut、字幕、平台适配与最后抛光 | 本地 FFmpeg（已实现）；Remotion / VectCut 为可选后端 | foryourhealth111-pixel/Vibe-Skills · Apache-2.0 |

> `ffmpeg-skill/` 内有两份 SKILL.md：仓库根的 `SKILL.md`（对应仓库根布局）和 `skills/ffmpeg-skill/SKILL.md`（插件安装版，按原仓库结构把脚本放在 `../../scripts/`）。两份都保留，目录层级也照搬，否则相对路径会失效。

## 依赖与适用边界（重要）

- **完全本地、无 API Key**：`ffmpeg-skill`（FFmpeg 6.1+ / Python 3.10+，纯标准库）、`ecommerce-video-skills/*`（ffmpeg + edge-tts + Pillow）、`video-studio`（本地 FFmpeg 后端）、`vlog-auto-edit`（系统级只需 ffmpeg，其余在 Python venv 内）。
- **需要外部凭证或云服务**：`youtube-clipper`（LLM 翻译）、`剪口播`（火山引擎 ASR）、`video-recap`（ASR / TTS）、`byted-mediakit/*`（火山引擎 mediakit，但 `process-tools` 带 `local_ffmpeg_tool.py` 本地回退）、`vectcut/*`（VectCutAPI 云端）、`easel-video-skills/*`（AI 生成零件）。使用前请看各自的 README / `.env.example`。
- **编排层技能**：`auto-short-video`、`video-editing`、`video-studio` 会调用同生态的其他技能或后端；其中 `video-studio` 的 Remotion / VectCut 后端在上游标注为 *planned / optional*，当前可用的是本地 FFmpeg 后端。`easel-video-skills/*` 源自 Easel 的 builtin 技能，脱离 Easel 后需自行补齐被调用的零件。
- **剪映相关**：`vectcut/skill/` 是云端 API 客户端（`vectcut_client.py`），`capcut-director/` 是编排层；`zenstory` 的 `video-recap` 另带剪映草稿模板（在 `references/jianying/`，含其独立的 `LICENSE.duo-video`）。
- **未收录二进制素材**：`Easel/clipify/assets/preview.png` 等演示图片、示例视频未复制，脚本与文档均完整。

## 文件规模

| 目录 | 文件数 | 体积 |
| --- | --- | --- |
| `skills/auto-video-editing/ffmpeg-skill/` | 63 | 2.42 MB |
| `skills/auto-video-editing/youtube-clipper/` | 17 | 0.10 MB |
| `skills/auto-video-editing/videocut-skills/` | 23 | 0.12 MB |
| `skills/auto-video-editing/ecommerce-video-skills/` | 10 | 0.06 MB |
| `skills/auto-video-editing/video-recap/` | 120 | 1.18 MB |
| `skills/auto-video-editing/easel-video-skills/` | 11 | 0.07 MB |
| `skills/auto-video-editing/byted-mediakit/` | 40 | 0.29 MB |
| `skills/auto-video-editing/vectcut/` | 6 | 0.07 MB |
| `skills/auto-video-editing/vlog-auto-edit/` | 8 | 0.10 MB |
| `skills/auto-video-editing/video-studio/` | 3 | 0.03 MB |
| `LICENSES/`（本批新增 10 份） | 10 | 0.05 MB |

## 与本仓库其他技能的配合

`skills/voiceover-script/`（口播稿结构 / 钩子 / 口语化）→ `skills/child-health/` 或 `skills/health-popular-science/`（科普事实底座）→ `skills/audio-script-writer/`（转成可听的口播稿）→ **`skills/auto-video-editing/`（自动剪辑成片）**。其中剪口播、去静音、字幕烧录、9:16 平台导出这几步都有对应技能。
