# PIPELINE_STATE · 乾隆刊武英殿本《御纂醫宗金鑑》

| 项 | 值 |
|---|---|
| book-slug | `yizong-jinjian` |
| 流水线 | RIA-TV++ v2.5 Bundle 版 |
| 当前阶段 | **阶段 5 完成，已交付** |
| 输出模式 | `single`（用户选「中医大师技能包」，跨会话单入口自动生效） |
| 安装位置 | `C://Users//majfn//.workbuddy//skills//yizong-jinjian-master//` |
| 编译产物 | `dist/yizong-jinjian-master/`（run-20261116-135000-3ba089） |
| 校验 | `validate_skill_pack.py`：0 errors / 0 warnings（25 个 .md，1 个 SKILL.md） |
| 用户红线 | 「能根据描述判定病因并提出真实可行治疗方案，同时列出依据来源，禁止臆断、杜撰、乱编」 |
| 最后更新 | 2026-11-16 |

## 阶段进度

| 阶段 | 状态 | 产出 |
|---|---|---|
| 0 整书理解 | ✅ | `BOOK_OVERVIEW.md`、`corpus/00-卷冊結構索引.md`、`corpus/0-首卷凡例.md` |
| 1 五路提取 | ✅ | `candidates/` 5 类候选池；4 路视觉转写 agent 产出 `corpus/A…D-*.md` |
| 1.5 三重验证 | ✅ | `verified.md`（12 通过）、`rejected/README.md`（5 淘汰） |
| 1.6 晋级门 | ✅ | `.cangjie/capabilities/destinations.json`（4 promoted / 8 router） |
| 2 RIA++ 能力卡 | ✅ | `.cangjie/capabilities/cards/` 12 张，每张 R/I/A1/A2/E/B 六段齐全 |
| 3 Zettelkasten | ✅ | `GLOSSARY.md`（20 条）、Bundle `also_read` |
| 4 压力测试 | ✅ | `test-prompts.json`（15 正例 + 3 互斥负例，含兄弟诱饵） |
| 5 编译交付 | ✅ | `DIGEST.md`、编译产物、技能包安装、资料库同步、本地版本化 |

## 关键决策记录

1. 源材料无文本层（60 个 PDF 均为 `PdfBuiltInPicture` 纯影印），禁止凭记忆蒸馏；改视觉逐页转写。
2. **逐字转写 125 图页**（首卷凡例 5 + 四路代表册 120），另 30 页首卷凡例/总目作结构核阅；全书约 3,900 图页，其余未转录，不得引用。
3. 溯源编号 `S<册号2位>-P<图页2位>`；引用须同时给册号、卷次、篇名。
4. 范围：用户初附 01–50（止于卷六十八），已扩展为全部 60 册。
5. **三处版心实证修正**（优先于通行著录）：
   - 伤寒心法要诀 36–39／杂病心法要诀 40–43（`S29-P01` 卷四十为杂病）
   - 妇科心法要诀册区间 31–34、幼科 35–38（`S34-P01` 卷四十九为妇科）
   - 册12 版心为「卷十七 正誤存疑篇」（`S12-P01`）
6. 安全边界优先于知识密度：阶段 0 批判产出写入 SKILL.md 与 CAP-12。
7. 四路转写均未屈从分派预设，按版心实录，差异已保留在语料备注与索引中。

## 已知阻塞

- GitHub 集成 `create_repository` 返回 403（集成无 Administration 写权限），且账号 `guanxinchn` 无可访问仓库可写；
  已改为本地 `git init` + 提交完成版本化，待用户创建空私有仓库或授予权限后推送。
