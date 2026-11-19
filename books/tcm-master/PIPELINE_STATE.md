# PIPELINE_STATE · 综合中医大师技能包（tcm-master）

| 项 | 值 |
|---|---|
| book-slug | `tcm-master` |
| 流水线 | RIA-TV++ v2.5 Bundle 版（多经典合集升级） |
| 当前阶段 | **阶段 0–5 完成，已交付** |
| 输出模式 | `single`（用户选「升级为综合中医大师」，单入口跨会话生效） |
| 目标入口 | `tcm-master`（保留 `yizong-jinjian-master` 作兼容） |
| Bundle | `.cangjie/capabilities/verified.yaml`（bundle_id `tcm-master-classics-2026-11-18`） |
| 用户红线 | 「提高诊断能力；禁止臆断、杜撰、乱编；列出依据来源」 |
| 建立日期 | 2026-11-18 |

## 阶段进度

| 阶段 | 状态 | 产出 |
|---|---|---|
| 0 整书理解 | ✅ | `corpus/00-经典总索引.md`（12 书坐标基准） |
| 1 五路转写 | ✅ | A 素问灵枢47、B 伤寒金匮47、C 脉学舌诊59、D 温病+衷中参西录64、E 函授讲解35 页；合计 252 页新转写 + 金鉴 125 = **377 页可引用** |
| 1.5 三重验证 | ✅ | 7 个新增能力单元通过 V1/V2/V3，见各卡审计信息 |
| 1.6 晋级门 | ✅ | `destinations.json`：19 active / 7 promoted / 12 router |
| 2 RIA++ 能力卡 | ✅ | 19 张（金鉴12 + 新增CAP-13~19），RIA六段齐全 |
| 3 Zettelkasten | ✅ | GLOSSARY 38 条（金鉴20 + 多经典18），`also_read` 已链接 |
| 4 压力测试 | ✅ | `test-prompts.json` 24 条（含兄弟诱饵与互斥负例） |
| 5 编译交付 | ✅ | single 入口 `tcm-master`，validate 0 errors/0 warnings；安装＋资料库＋GitHub 全部落地 |

## 关键决策记录

1. 用户 2026-11-18 选定：范围＝诊断四诊核心＋诊法专项＋温病与名医＋光明函授讲解本；形态＝升级为综合中医大师；深度＝结构精读＋核心原文抽读。
2. 本地 `古籍/` 205 册 + 光明函授 40 册 + 陈修园 28 册；抽查 11 册全部纯影印无文本层，只能渲染后目视转写。
3. 统一溯源编号 `<书代码>-P<页>`（如 `SJ-P06`），与金鉴 `S<册>-P<页>` 并存。
4. 金鉴 12 张能力卡全部继承；新增能力待转写后按 RIA++ 六段补充。
5. 讲解本明确标注「讲解本」，不得与原典混同引用。
6. 安全边界、出处随行、存疑不补、诸书互证为核心原则。

## 交付落地（全部完成 2026-11-18）

| 落点 | 状态 | 内容 |
|---|---|---|
| 用户级技能 | ✅ | `C:/Users/majfn/.workbuddy/skills/tcm-master/`，`agent_created: true`，40 文件 / 39 .md；validate 0 errors/0 warnings |
| 兼容保留 | ✅ | 原 `yizong-jinjian-master` 未动，可继续单独使用 |
| 语料与溯源 | ✅ | references/corpus/ 13 文件（12 古籍 + F 现代权威层）+ 语料覆盖与溯源索引（377 页图页层 + 11 条 MOD 层） |
| 资料库 | ✅ | 11 份：原 9 份 + 现代权威舌象层 MOD 语料 + CAP-20 舌形辨证卡 |
| GitHub | ✅ | `https://github.com/guanxinchn/zhongyi`（master；最新提交见下） |

## 2026-11-19 增补：现代权威来源层

- 触发：用户问"能否从网上查阅相关舌象的医学书籍完善本技能包"；确认方案为"新建独立来源层·分级标注 + 可参与辨证但随行出处"。
- 核准来源：《中医学》第9版（人卫2018，陈金水）望舌形 6 段；国家中医药管理局审核认证词条「裂纹舌」「为什么舌头中间有裂痕」「齿痕舌」；腾讯医典「齿痕舌」（辅助低权重）。均于 2026-11-19 WebFetch 逐字核准并留 URL。
- 新增：`corpus/F-现代权威舌象.md`（`MOD-CM9/SAT/YDX` 共 11 条）、CAP-20 `tixing-bianzheng` 卡、GLOSSARY +4 术语、test-prompts +4 用例。
- 规则：两层并存不混引；SKILL.md 核心原则第2、10条 + 加载规则 + 路由表已同步；`agent_created: true`、capability-count=20。
- 校验：validate 0 errors / 0 warnings；20 卡齐全；MOD 编号均可在 F 层回查。

## 待落地

全部完成。后续可选：扩大转录覆盖（本批 377 页为核心抽读，非全本）、按使用证据拆分 promoted 能力为独立 Skill、若需更多现代舌象/脉象可续补 `MOD-*` 层（须保持分级与可回查）。
