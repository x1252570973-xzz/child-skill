# 来源与许可（儿童健康科普专辑）

收录日期：2026-11-17。本目录下 30 个技能全部**原样复制**，未修改任何上游内容；仅按主题重新组织目录。

## 1. LeoYeAI/agent-master-skills

| 项 | 值 |
| --- | --- |
| 仓库 | https://github.com/LeoYeAI/agent-master-skills |
| 分支 | `main` |
| Star | 2199 |
| 许可证 | **MIT**（GitHub 已识别；原文见 [`LICENSES/LeoYeAI-agent-master-skills-MIT.txt`](../../LICENSES/LeoYeAI-agent-master-skills-MIT.txt)，Copyright (c) 2026 MyClaw.ai (LeoYeAI)） |
| 上游路径 | `skills/childcare-essentials/SKILL.md`、`skills/parenting-psychology/SKILL.md`、`skills/family-emergency-planning/SKILL.md` |
| 本仓库路径 | `skills/child-health/<同名目录>/SKILL.md` |

各 `SKILL.md` frontmatter 中保留了 `submitted_by`、`last_reviewed` 等作者信息。本仓库此前已从该仓库收录 `audio-script-writer`，许可证文件已存在。

## 2. runyuan-wang/nutrition-assistants

| 项 | 值 |
| --- | --- |
| 仓库 | https://github.com/runyuan-wang/nutrition-assistants |
| 分支 | `main` |
| Star | 9 |
| 许可证 | **MIT**（GitHub 已识别；根 LICENSE 原文见 [`LICENSES/runyuan-nutrition-assistants-MIT.txt`](../../LICENSES/runyuan-nutrition-assistants-MIT.txt)，Copyright (c) 2026 王润圆 Runyuan Wang）。`nutrition-risk-screening-calculator/` 另有独立 MIT LICENSE，已随包收录 |
| 收录包 | `child-obesity-food-guide-skill/`、`child-obesity-tcm-prevention-skill/`（含 `en/`、`ja/`）、`stunting-dietary-guide/`、`nutrition-risk-screening-calculator/` |
| 上游路径 | 与上述包同名，位于仓库根目录 |

依据的公开指南：

- 国家卫生健康委《儿童青少年肥胖食养指南（2024 年版）》
- 国家卫生健康委《儿童青少年生长迟缓食养指南（2023 年版）》
- 中华中医药学会《儿童青少年肥胖治未病干预指南》（2026）
- STRONGkids / STAMP 等儿童营养风险筛查量表

为保持技能可用，连同 `knowledge_base.md`、`recipes_data.md`、`system_prompt.md`、`kpk_*.md`、`src/*.py`、`references/scoring.md` 等支撑文件一并收录；仅省略了上游的安装脚本、测试与二进制示例文件。

## 3. yemugua/agent-skills

| 项 | 值 |
| --- | --- |
| 仓库 | https://github.com/yemugua/agent-skills |
| 分支 | `main` |
| Star | 0 |
| 许可证 | 仓库内 `LICENSE` 声明 "MIT License, Copyright (c) 2026"；**GitHub API 返回 `NOASSERTION`**，未被识别为标准 MIT 文本。再分发前建议向上游二次确认授权 |
| 上游路径 | `health/pediatric/<slug>/SKILL.md`、`health/kids/<slug>/SKILL.md`、`parenting/health/<slug>/SKILL.md` |
| 本仓库路径 | `skills/child-health/popular-science-templates/<slug>/SKILL.md` |

该仓库是超大型中文技能集合（约 2.9 万个 SKILL.md），儿童健康相关目录包括 `baby-care*`、`baby-feed`、`kids-care*`、`kids-health`、`kids-safety*`、`health/pediatric`、`health/kids`、`parenting/health` 等。本次只精选了**有实质要点与就医红线**的 23 篇，未收录大量空模板（如 `app-guides/` 下的占位式科普模板、`kids-care2/` 中与标题不符的模板）。

## 再分发说明

MIT 许可证要求保留版权声明与许可文本，因此三份上游 LICENSE 原文均放在 `LICENSES/`，且所有 `SKILL.md` 的 frontmatter（含 `name`、`description`、`license`、作者字段）保持原样。若上游更新，请对照本文件中的原始路径重新同步。
