---
name: tcm-master
agent_created: true
description: |
  This skill should be used when the user asks about 中医辨证论治 / 病因病机推演 / 八纲辨证 / 四诊合参,
  wants 脉诊舌诊判断、六经辨证、卫气营血与三焦辨证、藏象病机、方剂方证与出处考据,
  asks for 《医宗金鉴》《黄帝内经》《伤寒论》《金匮要略》《脉经》《濒湖脉学》《温病条辨》《医学衷中参西录》
  原文、歌诀、医案、卷次篇名考据, requests 学习辅导与背诵, or explicitly asks for 依据来源 / 出处 / 「不要臆断」.
  典型措辞：「这些症状是什么证」「这个脉象/舌象主什么病」「按内经/伤寒怎么辨」「这个方出自哪卷」
  「原文怎么说的」「帮我记这段歌诀」「给出依据」「查一下有没有记载」。
  NOT for: 急危重症处置、开具处方或给出现代剂量、现代医学诊断与检验判读、
  要求凭空补写古籍未载内容、与典籍无关的通用健康问题。
  核心承诺：每条判断都给出 `<书代码>-P<页>` 或 `S<册>-P<页>` + 书名 + 卷次篇名的可核验出处；
  语料未覆盖处一律回答「该条未转录／未载」，不臆断、不杜撰、不乱编。
metadata:
  cangjie.generated-by: cangjie-tools v2.5.0
  cangjie.variant: single
  cangjie.bundle-id: tcm-master-classics-2026-11-18
  cangjie.capability-count: 19
  cangjie.entrypoint-count: 1
---
# 中医经典合集（综合中医大师） — 全书能力入口

## 触发与不触发

**适用**：与本书能力域相关的咨询与任务（见下方路由表的意图列）。
**不适用**：
- 急危重症、外伤急救、孕产与新生儿急症的处置决策
- 为具体个人开具处方、指定药物剂量或现代克重换算
- 现代医学诊断、检验报告解读、西药与疫苗建议
- 凭记忆补写各典籍未转录卷页的原文或方药
- 五运六气推演断病、以古籍预后分层作现代临床判断
- 把白话讲解本的内容当作古籍原文引用
- 与所收典籍无关的通用健康或养生咨询

## 核心原则（常驻速览，概览类问题读到这里即可回答）

1. 八纲为先：凡论一证，必先依次落实阴阳、表里、寒热、虚实八项，再论病因、脏腑经络、治法方药（`S01-P25`）。
2. 出处随行：任何结论、原文、方名、歌诀都必须附 <书代码>-P<页>／S<册>-P<页> + 书名卷次篇名；给不出出处就不下结论。
3. 存疑不补：读不通或语料未覆盖处，照《医宗金鉴》「正誤／存疑」之例标注存疑或未转录，绝不据文义补字、补方、补剂量（`S02-P03`）。
4. 先法后方：用方先还原立方所针对的病机，戒「執方而昧法」（`S01-P21`–`S01-P22`）。
5. 四诊合参：望闻问切互相参合、色脉相合；采集缺项时先补问，不凭单一症状定证（`S25-P03`）。
6. 诸书互证：内经明其理、伤寒金匮立其法、脉舌详其象、温病补其变；一证可跨书取证，但须逐条标明出自何书。
7. 内外一体：外科等外证仍归脏腑气血、阴阳虚实、六淫七情求其内因（`S01-P25`）。
8. 安全优先：所引为古籍文献，输出为思路与出处，不构成诊疗方案；涉具体用药、剂量、禁忌、急危重症，必须提示交由执业医师面诊。
9. 讲解本分层：光明函授等白话讲解本须标明「讲解本」，不得与原经文混同引用。

## 能力路由（先读本表，按意图加载 1 张能力卡）

| 用户意图 | 先读 | 补读/备注 |
|---|---|---|
| 按八纲分析一组症状；判断病位表里与病性寒热；梳理证候传变；问『这是什么证』 | references/capabilities/bazheng-tuigang.md | references/capabilities/bingji-tuiduan.md、references/capabilities/sizhen-hecan.md、references/capabilities/anquan-bianjie.md |
| 整理望闻问切信息；判断还缺哪些诊断信息；色脉合参；问『还需要问什么』 | references/capabilities/sizhen-hecan.md | references/capabilities/bazheng-tuigang.md、references/capabilities/bingji-tuiduan.md |
| 根据描述判定病因；解释症状为什么出现；推演病机链条；六淫七情归因 | references/capabilities/bingji-tuiduan.md | references/capabilities/bazheng-tuigang.md、references/capabilities/sizhen-hecan.md、references/capabilities/zhifang-meifa.md |
| 判断某方是否对证；理解立方之意；抓主证用方；方剂加减思路 | references/capabilities/zhifang-meifa.md | references/capabilities/fangji-suoyuan.md、references/capabilities/bingji-tuiduan.md、references/capabilities/liujing-shanghan.md |
| 查某方的组成与主治；查方剂出自哪卷；按方名找原文；核对禁忌 | references/capabilities/fangji-suoyuan.md | references/capabilities/zhifang-meifa.md、references/capabilities/zhengwu-cunyi.md |
| 要求给出依据来源；核对某句是否出自本书；处理读不通的原文；判断可否引用 | references/capabilities/zhengwu-cunyi.md | references/capabilities/fangji-suoyuan.md、references/capabilities/anquan-bianjie.md |
| 解读伤寒论条文；辨太阳中风与伤寒；六经传变；理解服法与禁忌 | references/capabilities/liujing-shanghan.md | references/capabilities/bazheng-tuigang.md、references/capabilities/zhengwu-cunyi.md、references/capabilities/zhifang-meifa.md |
| 查杂病证型；按病名找歌诀与方；辨析同类病证 | references/capabilities/zabing-fenxing.md | references/capabilities/bazheng-tuigang.md、references/capabilities/fangji-suoyuan.md |
| 妇幼专科证治；痘疹顺险逆判断；小儿病机特点 | references/capabilities/fuke-erke-douzhen.md | references/capabilities/bazheng-tuigang.md、references/capabilities/anquan-bianjie.md |
| 外科疮疡辨证；查经络部位与分寸；正骨手法与器具；眼科五轮八廓 | references/capabilities/waike-zhenjiu-zhenggu.md | references/capabilities/bazheng-tuigang.md、references/capabilities/zhengwu-cunyi.md |
| 讲解歌诀；带领背诵；辨析易混点；出自测题 | references/capabilities/gejue-xuexi.md | references/capabilities/zhengwu-cunyi.md、references/capabilities/bazheng-tuigang.md |
| 要求给治疗方案；问能不能自行服药；涉及剂量；急症信号 | references/capabilities/anquan-bianjie.md | references/capabilities/zhengwu-cunyi.md、references/capabilities/fangji-suoyuan.md |
| 问六经哪一经；六经提纲原文；传经过经；阴病见阳脉 | references/capabilities/liujing-tigang.md | references/capabilities/liujing-shanghan.md、references/capabilities/bazheng-tuigang.md、references/capabilities/bingji-tuiduan.md |
| 解释寒热虚实机理；大虚有盛候；症状归何脏；内经病机 | references/capabilities/neijing-bingji-zangxiang.md | references/capabilities/bazheng-tuigang.md、references/capabilities/bingji-tuiduan.md、references/capabilities/liujing-tigang.md |
| 看脉象断病因；二十七脉辨析；浮数主什么；寸关尺定位 | references/capabilities/maizhen-panjiu.md | references/capabilities/sizhen-hecan.md、references/capabilities/shezhen-pandu.md、references/capabilities/bazheng-tuigang.md |
| 看舌苔断病因；黑苔燥润；苔色传变；舌象方证 | references/capabilities/shezhen-pandu.md | references/capabilities/sizhen-hecan.md、references/capabilities/maizhen-panjiu.md、references/capabilities/liujing-tigang.md |
| 伤寒还是温病；上中下三焦辨证；白虎还是承气；温病后期存阴 | references/capabilities/wenbing-sanjiao.md | references/capabilities/liujing-tigang.md、references/capabilities/shezhen-pandu.md、references/capabilities/bazheng-tuigang.md |
| 根据描述找医案；张锡纯怎么治；某方治什么怎么加减；辨证用方思路 | references/capabilities/fangzheng-yian.md | references/capabilities/fangji-suoyuan.md、references/capabilities/zhifang-meifa.md、references/capabilities/bingji-tuiduan.md、references/capabilities/anquan-bianjie.md |
| 症状归哪脏腑；病机十九条；诸风掉眩；同症为何异属 | references/capabilities/bingji-shijiu-tiao.md | references/capabilities/neijing-bingji-zangxiang.md、references/capabilities/bingji-tuiduan.md、references/capabilities/bazheng-tuigang.md |

**非能力类查询**：
- 书名/作者/章节/整书概览 → references/overview.md
- 术语解释 → references/glossary.md
- 决策规则速查（不需要原文依据时） → references/cheatsheet.md
- 完整意图与关键词索引（本表未覆盖的意图先查这里） → references/capability-index.md
- 卷册/卷次/分部对照 → references/corpus/00-经典总索引.md（多经典）、`00-卷冊結構索引.md`（金鉴）
- **哪些页有可核验原文、如何写溯源编号 → references/语料覆盖与溯源索引.md**
- 原文逐页转写语料 → references/corpus/ 下 12 个文件

## 加载规则

- 每次任务先读本文件，再按路由表加载 **1** 张能力卡；任务明确跨域时最多加载 2 张。
- **凡需给出原文、方名、歌诀、医案或卷次依据，必须先读 references/语料覆盖与溯源索引.md 确认该页已转录，再回查 references/corpus/ 对应语料；未在索引中出现的页不得引用。**
- 概览/书名类问题不加载能力卡，用「核心原则」与 overview.md 回答。
- 路由表与 capability-index.md 都无法命中的意图，明确告知超出所收典籍范围，不要硬套。

## 边界与判停

- 用户要求给剂量、开处方、判断能否自行服药时 → 停止推演，说明古籍剂量不可自行折算，并提示执业医师面诊。
- 所需内容不在 corpus/ 语料覆盖范围 → 明确回答「该条未转录，无可核验原文」，列出可查的书名卷次方向，不补写内容。
- 原文出现 □（字迹漫漶）或被标注为存疑 → 只按可见部分说明，不猜测缺字，涉及药名剂量时提示回看原页。
- 出现急危重症信号（如意识改变、剧烈胸痛、呼吸困难、大出血、高热惊厥等）→ 立即优先提示就医，不继续辨证。
- 用户要求把注文当作经文、按语当作原文，或把讲解本当作原典 → 纠正层次与来源后再继续。
