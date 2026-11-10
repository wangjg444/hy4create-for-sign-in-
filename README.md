# JavaScript 学习与复习手册

一份**兼顾「第一次学懂」和「考前快速回看」**的 JavaScript 教学资料，交付形式为 22 页 PPTX。

- **成品**：`JavaScript学习与复习手册.pptx`（1280×720，共 22 页，约 84 KB）
- **定位**：可长期回看的知识地图，不是一次性汇报课件
- **受众**：已接触 HTML/CSS、正在入门或阶段复习 JavaScript 的学习者
- **范围**：ES2015+ 核心语法、函数与作用域、异步运行时、DOM 事件；不含框架、TypeScript、工程化
- **素材**：全部文字、代码、图示为原创内容，无外部图片与第三方素材依赖

---

## 快速开始

| 你想做什么 | 怎么做 |
| --- | --- |
| 系统学一遍 | 从 P1 顺序看到 P17，每页标题就是结论，代码块可复制到浏览器控制台或 Node 直接运行 |
| 考前 / 面试前复习 | 只看 P18–P21：易错点 → 自测题 → 答案解析 → 一页纸速查 |
| 打印随身带 | 单独打印 P21，三分钟扫完声明 / 类型 / 数组 / 异步四组规则 |
| 按错题回看 | P18、P20 每条都标了对应知识页页码，只翻那一页即可 |
| 打开文件 | PowerPoint、WPS、腾讯文档均可直接打开，无需安装任何依赖 |

> 阅读端不需要 Node、不需要联网。只有**修改源文件并重新生成 PPT** 时才需要构建环境（见「修改与再生成」）。

---

## 目录结构

```
D:\workbuddy工作空间\2026-11-10-14-40-48\        ← 工作区根
├─ .slidep\                                      # slidep 命令日志 / 临时导出（自动生成）
├─ .workbuddy\                                   # 工作区记忆，与内容无关
└─ JavaScript学习与复习\                          ← 本项目根目录
   ├─ README.md                                  # 本文件
   ├─ DESIGN.md                                  # 设计契约：配色、字号、母版、逐页字段表
   ├─ JavaScript学习与复习手册.pptx               # 交付成品
   ├─ slides\                                    # 22 个页面源文件（slidep DSL）
   │  ├─ 01.slide … 22.slide
   │  └─ …
   └─ assets\                                    # 预留素材目录，当前为空（全篇未使用外部图片）
```

`NN.slide` 与 PPT 第 `NN` 页一一对应；PPT 本身是**生成产物**，改内容应改 `.slide` 源文件后重新写入。

---

## 内容地图

四个章节 + 复习闭环，章节扉页分别为 P4 / P8 / P13 / P17，编号与 P2 目录页严格对应。

| 章节 | 页码区间 | 内容 |
| --- | --- | --- |
| 01 语法与数据基础 | P4–P7 | const/let/var、7 种原始类型与 typeof 三个特例、隐式转换与 `===`、真假值 |
| 02 函数与作用域 | P8–P12 | 四种函数写法、this 四条绑定规则、闭包、数组/对象方法速查、解构/展开/可选链 |
| 03 异步与运行时 | P13–P16 | 事件循环与输出顺序、Promise 三态与 async/await、DOM 与事件委托 |
| 04 复习与自测 | P17–P21 | 八条高频易错点、六道输出题、逐题解析、一页纸速查 |

> 区间含章节扉页，例如 01 的扉页是 P4，知识页是 P5–P7。

### 逐页索引

| 页 | 标题 | 类型 | 作用 |
| --- | --- | --- | --- |
| 01 | JavaScript 学习与复习手册 | 封面 | 范围、关键词、适用对象 |
| 02 | 目录 CONTENTS | 目录 | 四章与页码区间 |
| 03 | 这份资料怎么用：学一遍、查一遍、测一遍 | 使用说明 | 学习线四步 + 复习线 |
| 04 | 01 语法与数据基础 | 章节页 | — |
| 05 | 变量声明：默认 const，需要重赋值才用 let | 知识页 | 作用域 / 提升 / TDZ 对照、选择顺序 |
| 06 | 数据类型与 typeof 速查 | 速查页 | 类型分类图 + typeof 结果表 |
| 07 | 类型转换与相等判断：一律用 === | 知识页 | 隐式转换典型式、8 个假值 |
| 08 | 02 函数与作用域 | 章节页 | — |
| 09 | 函数、箭头函数与 this：四条绑定规则 | 知识页 | 四种写法 + this 绑定矩阵 |
| 10 | 闭包：函数记住了它出生的环境 | 重点页 | 三层作用域链图示 + 计数器代码 |
| 11 | 数组与对象：高频操作速查 | 速查页 | 标出哪些方法改变原数组 |
| 12 | 解构、展开与可选链：写短，也要写对 | 知识页 | 默认值、rest、浅拷贝、`?.` 与 `??` |
| 13 | 03 异步与运行时 | 章节页 | — |
| 14 | 事件循环：同步 → 微任务 → 宏任务 | 重点页 | 全流程链 + 实际输出顺序 |
| 15 | Promise 与 async/await：错误也要有出口 | 知识页 | 三态、try/catch、all 与 allSettled |
| 16 | DOM 与事件委托：一个监听器管住所有子元素 | 知识页 | 捕获/冒泡、委托写法 |
| 17 | 04 复习与自测 | 章节页 | — |
| 18 | 八个高频易错点：每条都给出处 | 复习页 | 每条给正确做法与回看页码 |
| 19 | 自测：先写答案，再看下一页 | 自测页 | 6 道短代码输出题，不预给答案 |
| 20 | 答案与解析：错在哪，比答案更重要 | 解析页 | 逐题输出 + 一句原理 + 回看页码 |
| 21 | 一页纸速查表：三分钟扫完核心语法 | 速查页 | 声明 / 类型 / 数组 / 异步四组 |
| 22 | 把知识留下来的是重复，不是看懂 | 封底 | 1 天 / 3 天 / 7 天复习节奏 |

---

## 学习线与复习线怎么配合

**学习线（P3–P16）**：概念 → 代码 → 对照 → 自测。每页标题写结论而非主题名，正文配可运行代码、对照表或关系图；相邻页版式不重复，重点页（P10、P14）用大图示承担视觉。

**复习线（P18–P22）**：先暴露问题再回看，避免「看懂了」的错觉。

1. P18 八条易错点，逐条自问能否说出正确做法；
2. P19 遮住下一页，独立写出 6 道题的输出；
3. P20 对答案，错在哪比答案重要，按标注页码回看原始知识页；
4. P21 单独打印，作为考前最后一瞥；
5. P22 按 1 天 / 3 天 / 7 天间隔重做，而不是当天连刷三遍。

---

## 设计规范摘要

完整约定见 `DESIGN.md`，改动版式前请先读它。

| 槽位 | 色值 | 用途 |
| --- | --- | --- |
| 主色 | `#2563EB` | 编号、章节大字、主色块 |
| 辅色 | `#06B6D4` | 次级序列、流程辅线 |
| 强调色 | `#F59E0B` | 关键结论、警示、答案标记（每页 2–3 处） |
| 正文 / 次要 | `#1E293B` / `#64748B` | 文字 |
| 线 / 浅底 | `#E2E8F0` / `#EFF6FF` | 分隔线、卡片底 |
| 深色代码面板 | `#0F172A` | 代码块、深色块 |

- 画布 1280×720，内容页 padding 60，安全区 1160×600
- 字体：中文 Microsoft YaHei，西文 Arial，代码块使用等宽字体（唯一例外）
- 字号阶梯：页面主标 36 / 卡片小标 24 / 正文 18–20 / 表格 16 / 页脚 14，可见文字不小于 14px
- 内容页统一母版：左上角 24×8 主色小条 + 36px 主标题 + 1px 贯通细线 + 固定页脚（左侧章节名、右侧页码）；封面、目录、章节页、封底不加页脚
- 全篇禁用阴影、渐变、emoji、装饰性照片；深色大块每页不超过 1 个

---

## 修改与再生成

编辑端需要 **WorkBuddy 内置 `slidep` CLI**（Node 22 托管环境，`/c/Users/user/.workbuddy/binaries/node/versions/22.22.2-6/slidep`）。
`create` 与 `upsert-dsl` 依赖本地 editor_sdk（默认 `http://localhost:39099`）；`lint` 是纯本地布局检查，不依赖服务。

在本项目根目录执行：

```bash
# 1) 修改单个页面后，替换第 5 页（--page-index 是 0-based，5 页 → 4）
slidep upsert-dsl "JavaScript学习与复习手册.pptx" --dsl-file "slides/05.slide" --page-index 4

# 2) 每页写完立刻做布局检查
slidep lint "JavaScript学习与复习手册.pptx" --dsl-file "slides/05.slide" --page-index 4

# 3) 从零按 01→22 顺序重建整份 PPT
slidep create "JavaScript学习与复习手册.pptx"
for i in $(seq -w 1 22); do
  slidep upsert-dsl "JavaScript学习与复习手册.pptx" --dsl-file "slides/${i}.slide"
  slidep lint "JavaScript学习与复习手册.pptx" --dsl-file "slides/${i}.slide" --page-index $((10#$i - 1))
done

# 4) 把成品导出成 Markdown，用于核对文字内容
slidep inspect "JavaScript学习与复习手册.pptx" --out "./check.md"
```

要点：

- `upsert-dsl` **省略 `--page-index` 表示追加到末尾**，指定则替换该页；页面顺序由写入顺序决定，因此插入中间页后需重建其后的所有页。
- `create` 用于新建空文件；从零重建前请先备份或移走现有 `pptx`。
- `lint` 报 `no-overflow` / `component-overlap` / `child-containment` 等 error 时退出码为 1，必须修到 `diagnostics: []` 再继续。
- `inspect --out` 不会覆盖已有文件，重新导出请换一个新路径。

### DSL 页面骨架

每页是一个 `.slide` 文件，语法为 JSX 风格的 Box / Text / CodeBlock / Table / SVG 组合：

```jsx
<Slide style={{ width: 1280, height: 720, padding: 60, background: '#FFFFFF',
                position: 'relative', fontFamily: 'Microsoft YaHei, Arial' }}>
  <Box style={{ width: 1160, height: 60, flexDirection: 'column' }}>
    <Box style={{ flexDirection: 'row', alignItems: 'center', gap: 12, height: 52 }}>
      <Box style={{ width: 24, height: 8, borderRadius: 4, background: '#2563EB' }} />
      <Text style={{ fontSize: 36, fontWeight: 'bold', color: '#1E293B', lineHeight: 1.2 }}>页面标题写结论</Text>
    </Box>
    <Box style={{ width: 1160, height: 1, background: '#E2E8F0', marginTop: 7 }} />
  </Box>
  <Box style={{ width: 1160, height: 528, flexDirection: 'row', gap: 24, marginTop: 12 }}>
    <CodeBlock code={`const PI = 3.14;`} language='javascript' width={700} fontSize={16} />
  </Box>
  <Box style={{ position: 'absolute', top: 668, left: 60, width: 1160, height: 24,
                flexDirection: 'row', justifyContent: 'space-between' }}>
    <Text style={{ fontSize: 14, color: '#64748B', lineHeight: 1.4 }}>JavaScript · 学习与复习　章节名</Text>
    <Text style={{ fontSize: 14, color: '#64748B', lineHeight: 1.4 }}>05</Text>
  </Box>
</Slide>
```

---

## 维护注意事项

- **花括号转义**：DSL 中作为普通文字出现的 `{`、`}` 必须写成字符串表达式，例如 `{'{...user}'}`，直接写会被当成 JSX 表达式导致解析失败。
- **中文溢出**：固定高度卡片里中文换行比预估多一行，高度要留余量；以 `lint` 诊断为准，不要凭肉眼判断。
- **编号一致性**：新增/删除页面时，必须同步更新 P2 目录页码区间、P4/P8/P13/P17 章节页的页码区间、每页页脚页码，以及 `DESIGN.md` 的「章节与目录契约」和逐页字段表。
- **写作纪律**：标题写结论不写「XX 介绍」；代码块必须能实际运行且注释写清输出；复习页不留悬念，必须给答案或正确做法；全篇不出现 emoji、感叹号、形容词堆砌标题。
- `assets/` 目前为空，若引入图片需同步更新 `DESIGN.md` 的配图清单；`.slidep/` 是命令日志缓存，不需要纳入版本管理。

---

## 已知范围与可扩展方向

当前版本聚焦「语法 → 函数 → 异步 → 自测」这条主线，以下内容**没有覆盖**：原型链与继承的实现细节、ES Module 与打包、TypeScript、浏览器存储与网络请求（fetch）、正则、性能优化、测试与框架。

若要扩展，建议按现有结构追加新章节：在 `slides/` 增加连续编号的 `.slide` → 更新目录页与章节页 → 同步 `DESIGN.md` 契约 → 在 P18/P19 补对应易错点与自测题 → 全量 `lint` 后重建。

---

## 版本记录

| 日期 | 版本 | 说明 |
| --- | --- | --- |
| 2026-11-10 | v1.0 | 初版，22 页，4 章 + 复习闭环；全篇通过逐页布局检查 |
| 2026-11-10 | 文档 | 新增 `README.md` 与目录结构说明，PPT 内容未改动 |
