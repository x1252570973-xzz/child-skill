# 儿童健康科普技能索引

本次新增 **30 个技能 / 75 个上游文件**（另含 1 份上游 LICENSE 放在 `LICENSES/`、2 份本仓库索引文档，合计 78 个新文件），来自 3 个上游仓库。所有上游文件原样收录，未修改内容；归属与许可证见 [SOURCE.md](SOURCE.md)，全库说明见 [../../README.md](../../README.md)。

> ⚠️ 儿童健康内容仅供科普与教育，不构成诊疗建议。**儿童用药剂量必须按体重并遵医嘱**；3 月龄以下婴儿发热、热性惊厥、呼吸困难、皮疹压不褪色等情形请立即就医。各技能内均保留了上游的「红线 / 就医提示」，使用时请勿删改。

## 一、完整照护与心理指南（3 个 · MIT）

| 目录 | 主题 | 类型 | 来源 / 许可 |
| --- | --- | --- | --- |
| `childcare-essentials` | 0–5 岁婴幼儿日常照护实操（喂养、睡眠、安抚、换洗、居家安全） | 完整技能包 · 英文 | LeoYeAI/agent-master-skills · MIT |
| `parenting-psychology` | 0–18 岁情绪与发育引导、分龄期望、管教策略、青春期大脑 | 完整技能包 · 英文 | LeoYeAI/agent-master-skills · MIT |
| `family-emergency-planning` | 家庭应急预案：备灾物资、儿童随行包、失联联络与避险演练 | 完整技能包 · 英文 | LeoYeAI/agent-master-skills · MIT |

这 3 个是英文长篇技能包（每个约 2.1–2.6 万字符），内容自洽、可直接作为 Agent 技能使用，适合做家长问答、科普长文或口播稿的事实底座。

## 二、循证儿童营养与筛查（4 个 · MIT）

| 目录 | 主题 | 类型 | 来源 / 许可 |
| --- | --- | --- | --- |
| `child-obesity-food-guide-skill` | 儿童青少年肥胖食养（国家卫健委《儿童青少年肥胖食养指南（2024 年版）》；14 个 KPK 知识点、5 地区 24 天食谱、10 个营养方） | 完整技能包 · 中文 | runyuan-wang/nutrition-assistants · MIT |
| `child-obesity-tcm-prevention-skill` | 儿童青少年肥胖治未病（中华中医药学会 2026 干预指南；13 个 KPK、7 种体质、4 种证型、四期干预；含 en/ja 版本） | 完整技能包 · 中/英/日 | runyuan-wang/nutrition-assistants · MIT |
| `stunting-dietary-guide` | 儿童青少年生长迟缓食养（国家卫健委《儿童青少年生长迟缓食养指南（2023 年版）》；13 个 KPK、5 地区 15 套食谱、9 个食养方） | 完整技能包 · 中文 | runyuan-wang/nutrition-assistants · MIT |
| `nutrition-risk-screening-calculator` | 营养风险筛查计算器：内置 STRONGkids（儿童）、STAMP、NRS-2002、MUST 量表，可运行 Python CLI 输出风险等级与处置建议 | 完整技能包 · 中文 + Python | runyuan-wang/nutrition-assistants · MIT |

依据均为公开发布的国家 / 学会指南，附带知识库、食谱数据、系统提示词与可运行代码，是本次收录中**信息密度最高**的一组。`nutrition-risk-screening-calculator` 自带 MIT LICENSE，其余沿用仓库根 LICENSE。

```bash
# 儿童营养风险筛查（STRONGkids）
python skills/child-health/nutrition-risk-screening-calculator/src/cli.py --help
```

## 三、中文儿童健康科普速查（23 个 · 轻量模板）

来自 `yemugua/agent-skills`，每个约 450–810 字符，采用「核心要点 → 常见误区 → 就医红线」结构，适合做短视频口播稿骨架、家长问答要点或科普推文提纲。目录名保留上游 slug。

| 目录 | 主题（取自 SKILL.md frontmatter） | 上游原始路径 |
| --- | --- | --- |
| `ertong-faxingjuejue` | 热性惊厥 | `health/kids/ertong-faxingjuejue/SKILL.md` |
| `ertong-jinshi-fangkong` | 儿童近视防控实操 | `health/kids/ertong-jinshi-fangkong/SKILL.md` |
| `ertong-shengao-guanli` | 儿童身高科学管理 | `health/kids/ertong-shengao-guanli/SKILL.md` |
| `youer-jizhen` | 幼儿急疹 | `health/kids/youer-jizhen/SKILL.md` |
| `ertong-fashao-chuli` | 儿童发热家庭处理 | `health/pediatric/ertong-fashao-chuli/SKILL.md` |
| `ertong-fashao` | 儿童发烧处理 | `health/pediatric/ertong-fashao/SKILL.md` |
| `ertong-fuxie` | 儿童腹泻与补液 | `health/pediatric/ertong-fuxie/SKILL.md` |
| `ertong-keshou` | 儿童咳嗽与呼吸道 | `health/pediatric/ertong-keshou/SKILL.md` |
| `ertong-shili-bk` | 视力 | `health/pediatric/ertong-shili-bk/SKILL.md` |
| `ertong-shili` | 儿童视力与近视防控 | `health/pediatric/ertong-shili/SKILL.md` |
| `ertong-shizheng` | 儿童视力筛查 | `health/pediatric/ertong-shizheng/SKILL.md` |
| `ertong-shuimian` | 儿童睡眠 | `health/pediatric/ertong-shuimian/SKILL.md` |
| `ertong-tiyan` | 儿童体检与发育筛查 | `health/pediatric/ertong-tiyan/SKILL.md` |
| `ertong-tizhong` | 儿童体重管理 | `health/pediatric/ertong-tizhong/SKILL.md` |
| `ertong-yali` | 儿童焦虑与情绪 | `health/pediatric/ertong-yali/SKILL.md` |
| `paozhen-yanxia-yan-tou` | 疱疹性咽峡炎 | `health/pediatric/paozhen-yanxia-yan-tou/SKILL.md` |
| `tuishao-yongyao` | 儿童退烧用药指南 | `health/pediatric/tuishao-yongyao/SKILL.md` |
| `youer-fashao-jieti` | 幼儿发烧 | `health/pediatric/youer-fashao-jieti/SKILL.md` |
| `baobao-fatiao` | 宝宝发烧处理 | `parenting/health/baobao-fatiao/SKILL.md` |
| `baobao-kosou` | 宝宝咳嗽处理 | `parenting/health/baobao-kosou/SKILL.md` |
| `baobao-shizhen` | 宝宝湿疹 | `parenting/health/baobao-shizhen/SKILL.md` |
| `haizi-pinqian` | 孩子挑食矫正 | `parenting/health/haizi-pinqian/SKILL.md` |
| `haizi-shuomian` | 孩子说话晚评估 | `parenting/health/haizi-shuomian/SKILL.md` |

### 上游已知问题（原样保留，未修正）

- 少数 slug 与实际主题不一致：例如 `ertong-shizheng` 内容是「儿童视力筛查」而非湿疹、`ertong-shili-bk` 是「视力保护与近视防控」。索引按 frontmatter 的 `description` 标注，目录名不改，便于对照上游。
- 部分文件的 Markdown 加粗嵌套有破损（多余的 `**` 与括号），属上游生成格式问题，不影响要点阅读。
- 主题有重叠（3 篇发热、3 篇视力/近视、2 篇咳嗽），切入角度不同，按需要择一使用。
- 该仓库 GitHub API 返回 `NOASSERTION`（LICENSE 仅写 "MIT License / Copyright (c) 2026"），再分发前建议二次确认授权，详见 [SOURCE.md](SOURCE.md)。

## 文件规模

| 来源 | 技能数 | 文件数 | 字符数（约） |
| --- | --- | --- | --- |
| LeoYeAI/agent-master-skills | 3 | 3 | 69,000 |
| runyuan-wang/nutrition-assistants | 4 | 49 | 169,000 |
| yemugua/agent-skills | 23 | 23 | 14,000 |
