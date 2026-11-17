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
| 最后更新 | 2026-11-17 |

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

## 交付落地

| 落点 | 状态 | 内容 |
|---|---|---|
| 用户级技能 | ✅ | `C://Users//majfn//.workbuddy//skills//yizong-jinjian-master//`，`agent_created: true`，25 个 .md |
| 本地版本化 | ✅ | `yizong-jinjian/.git`，56 个文本文件、6734 行插入；`pages/`、`_probe/`、PNG 已忽略 |
| 资料库 | ✅ | 个人空间，11 个 doc：DIGEST、整书理解、术语词典、卷册索引、语料覆盖与溯源索引、SKILL.md 入口、首卷凡例、原文语料 A/B/C/D；语义检索已回查命中 |
| GitHub 仓库 | ✅ | `https://github.com/guanxinchn/zhongyi`（Public，master 分支，2 提交 / 56 文件已推送并 API 复核） |

资料库 11 个文档的链接（均由上传返回）：

- 精华总览与交付说明 `https://www.workbuddy.cn/space/d/TgwOA8peDjgCIMZBqIkoHH`
- 整书结构理解 `https://www.workbuddy.cn/space/d/KKOVXP7ot2bxLN1gMx8Ho0`
- 术语词典 `https://www.workbuddy.cn/space/d/QUI0EW1237ly5NNuxWxGXv`
- 卷册结构与溯源坐标 `https://www.workbuddy.cn/space/d/ekZejh7AmIYzjsUdpnhso3`
- 已转录语料覆盖与溯源索引 `https://www.workbuddy.cn/space/d/L7ALjNhw6pwklYOvStJE34`
- 中医大师技能包入口 `https://www.workbuddy.cn/space/d/6siJP6aqVRlTwYp9TLc8GG`
- 原文语料·首卷凡例 `https://www.workbuddy.cn/space/d/wo8v0LfRHyLEbZdd0dWRpV`
- 原文语料 A 诊法方论伤寒 `https://www.workbuddy.cn/space/d/ZhGklWmCk3TYxB2uxFQp1i`
- 原文语料 B 仲景全书 `https://www.workbuddy.cn/space/d/5TjRR72zHDVKw37nufaSAD`
- 原文语料 C 杂病妇幼痘疹 `https://www.workbuddy.cn/space/d/P6v8PoNDeWQ0ygmDzuglCO`
- 原文语料 D 外科眼科刺灸正骨 `https://www.workbuddy.cn/space/d/hUsmdJCnwwyarllxTDz8xb`

## 遗留说明（已解决 / 固有限制）

- GitHub 建仓：集成 `create_repository` 始终 403（无 Administration 写权限），改由用户手工建空仓库
  `guanxinchn/zhongyi`（Public）。集成写文件亦 403（缺 Contents: write），重新授权后 token 失效，
  最终由用户在本地 Git Bash 完成浏览器授权 + `git push`（清除失效代理 `127.0.0.1:8412` 后直连通）。
  2026-11-17 15:13 推送成功：远端 master HEAD `f364953`，API `git/trees` 复核 56 个 blob 全部到位。
- 全书约 3,900 图页，仅逐字转写 125 页；技能包被设计为对未覆盖页明确回答「本书该条未转录，无可核验原文」。
  如需全文级覆盖，须另做全本转写。
