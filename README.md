# Perovskite Tandem Research Skill（中文介绍）

## 简介

`perovskite-tandem-research` 是一个面向钙钛矿与叠层太阳能电池方向的研究分析 Skill。它用于支持学术文献精读、研究方向扫描、效率纪录核查、技术路线评估、实验设计、产业化分析、竞品/机构动态跟踪，以及公司或研究机构层面的研发决策。

该 Skill 的核心定位不是建立一个会快速过期的静态论文库，而是提供一套可复用的领域分析框架、代表性文献地图、指标解释、稳定性评价标准、技术路线评估方法和动态联网核查规则。

## 适用场景

适合用于以下任务：

- 精读钙钛矿太阳能电池、钙钛矿/硅叠层、全钙钛矿叠层等方向的论文
- 总结某一研究方向的最新进展、热点和技术瓶颈
- 比较 2T 与 4T 叠层路线、钙钛矿/硅与全钙钛矿叠层路线、溶液法与蒸镀法等技术路径
- 核查最新效率纪录、认证效率、公司公告和产业化动态
- 设计实验验证方案、测试矩阵、稳定性测试方案和 Go/No-Go 标准
- 为公司、实验室或研究机构提供内部研发决策支持
- 跟踪 Oxford PV、LONGi、HZB、KAUST、NREL、Fraunhofer ISE 等公司和研究机构的公开进展

## 主要工作模式

### 1. paper-review：论文精读

用于分析上传论文、指定标题、DOI 或用户提到的“这篇论文”。默认输出包括：

- 一句话结论
- 研究背景
- 器件结构
- 关键创新
- 性能数据
- 稳定性分析
- 数据可信度
- 可复现性判断
- 产业化相关性
- 对研发决策的启发
- 建议验证实验

### 2. research-scan：研究方向扫描

用于回答某个方向的最新进展、研究热点和未来机会。默认输出包括：

- 总体判断
- 最新进展
- 技术热点
- 核心瓶颈
- 代表论文
- 代表机构/公司
- 产业化信号
- 值得跟进的问题
- 暂缓跟进的问题

涉及“最新”“最近”“当前”“今年”“效率纪录”“公司动态”等问题时，Skill 要求联网查证。

### 3. route-evaluation：技术路线评估

用于比较不同技术路线，例如：

- perovskite/silicon 2T tandem
- perovskite/silicon 4T tandem
- all-perovskite tandem
- perovskite/CIGS tandem
- wide-bandgap perovskite top cell
- Sn-Pb low-bandgap bottom cell
- slot-die coating
- vapor deposition
- textured silicon compatible process

默认输出包括路线对比、效率潜力、稳定性风险、工艺兼容性、放大制造难度、成本与设备需求、竞争格局和推荐优先级。

### 4. rd-decision：研发决策

用于公司、实验室或研究组进行方向选择、项目立项和资源优先级判断。默认输出：

- Go / Conditional Go / Watch / No-Go 结论
- 关键假设
- 关键风险
- 资源需求
- 3 个月验证实验
- 6 个月里程碑
- Go/No-Go 标准

### 5. experiment-planning：实验设计

用于把论文、技术路线或研发问题转化为可执行实验方案。默认输出：

- 实验目标
- 核心假设
- 样品结构
- 变量设计
- 对照组
- 制备流程
- 表征项目
- 稳定性测试
- 成功标准
- 失败判据
- 备选方案

### 6. competitor-watch：竞品与产业动态跟踪

用于跟踪公司、研究机构、认证效率、组件进展、产线状态和商业化动态。该模式必须联网查证，不依赖静态参考资料作为最终事实依据。

## 目录结构

```text
perovskite-tandem-research/
├── SKILL.md
├── README_CN.md
├── README_EN.md
├── agents/
│   └── openai.yaml
└── references/
    ├── workflow.md
    ├── literature-map.md
    ├── key-papers.md
    ├── literature-update-rules.md
    ├── paper-review-template.md
    ├── technology-routes.md
    ├── route-evaluation-framework.md
    ├── rd-decision-framework.md
    ├── experiment-planning.md
    ├── stability-assessment.md
    ├── metrics-glossary.md
    ├── source-priority.md
    ├── competitor-watchlist.md
    ├── manufacturing-and-scaleup.md
    ├── go-no-go-scorecard.md
    └── report-template.md
```

## 参考资料说明

- `workflow.md`：任务模式识别和路由逻辑
- `literature-map.md`：钙钛矿与叠层太阳能电池领域文献地图
- `key-papers.md`：代表性论文卡片库
- `literature-update-rules.md`：文献检索、筛选、更新和引用规则
- `paper-review-template.md`：论文精读模板
- `technology-routes.md`：技术路线知识库
- `route-evaluation-framework.md`：技术路线评估框架
- `rd-decision-framework.md`：内部研发决策框架
- `experiment-planning.md`：实验设计模板
- `stability-assessment.md`：稳定性与可靠性评价规则
- `metrics-glossary.md`：光伏和叠层电池指标解释
- `source-priority.md`：信息来源优先级和可信度规则
- `competitor-watchlist.md`：重点公司和研究机构跟踪清单
- `manufacturing-and-scaleup.md`：制造、组件和放大检查清单
- `go-no-go-scorecard.md`：Go/No-Go 加权评分表
- `report-template.md`：研究报告和决策报告模板

## 核心判断原则

该 Skill 在分析时会强制区分：

- 认证效率 vs 自报效率
- active area vs aperture area vs designated illumination area vs module area
- scan PCE vs stabilized PCE vs MPP-tracked output
- 实验室小面积电池 vs minimodule vs 商业组件
- 短期存储稳定性 vs 运行可靠性
- 未封装稳定性 vs 封装后稳定性
- 室内 STC 结果 vs 户外 energy yield
- 论文结果 vs 可制造工艺
- 公司公告 vs 第三方认证结果

## 使用示例

可以这样提问：

```text
帮我精读这篇钙钛矿/硅叠层论文，重点看创新点、稳定性和可产业化价值。
```

```text
比较 2T 和 4T 钙钛矿/硅叠层路线，给出研发优先级和 Go/No-Go 判断。
```

```text
最近全钙钛矿叠层太阳能电池有什么重要进展？请区分论文进展和产业化进展。
```

```text
根据这篇论文设计一个 3 个月的宽带隙钙钛矿顶电池验证实验。
```

```text
跟踪 Oxford PV 和 LONGi 在钙钛矿/硅叠层方向的最新公开进展，并判断可信度。
```

## 重要限制

- 静态参考资料仅用于分析框架、术语解释和代表性文献线索，不代表最新事实。
- 涉及最新论文、效率纪录、认证状态、公司动态和产业化状态时，必须联网查证。
- 公司新闻稿和营销材料不能直接等同于第三方认证或产业化成熟。
- 论文中的高效率小面积器件不能直接等同于可量产组件。
- 本 Skill 不包含任何特定公司的内部信息，除非用户在当前对话中明确提供。

## 安装与部署说明

本 Skill 的标准交付物是 `perovskite-tandem-research.zip`。不同 Agent 工具对 Skill 的支持方式不同：有些工具可以直接上传 ZIP，有些工具需要把 `SKILL.md` 和 `references/` 文件作为知识库、项目说明或系统提示导入。

### 1. ChatGPT Skills 原生安装

适用于支持 Skills 上传的 ChatGPT 工作区。

1. 打开 ChatGPT 的 Skills 管理页面或工作区中的 Skills Library。
2. 选择上传或创建 Skill。
3. 上传 `perovskite-tandem-research.zip`。
4. 确认 Skill 名称为 `perovskite-tandem-research`。
5. 安装完成后，使用下面的问题测试：

```text
帮我比较钙钛矿/硅 2T tandem 和 all-perovskite tandem 的研发优先级。
```

如果 Skill 正常触发，回答应包含技术路线比较、稳定性风险、产业化判断和 Go / Conditional Go / Watch / No-Go 结论。

### 2. ChatGPT Custom GPT / GPT Builder

Custom GPT 通常不能直接把 Skill ZIP 当作原生 Skill 运行，但可以把它作为知识文件和指令源使用。

建议步骤：

1. 解压 `perovskite-tandem-research.zip`。
2. 在 GPT Builder 中创建新的 GPT。
3. 将 `SKILL.md` 的核心行为规则复制到 Instructions。
4. 将 `references/` 下的 Markdown 文件上传到 Knowledge。
5. 可选：上传 `README_CN.md` 和 `README_EN.md` 作为用户说明。
6. 在 Capabilities 中开启 Web browsing / Search（如可用），因为该 Skill 要求核查最新论文、效率纪录和公司动态。
7. 用以下问题测试：

```text
Oxford PV 和 LONGi 在钙钛矿/硅叠层方向的最新公开进展是什么？请区分自报信息和第三方认证信息。
```

### 3. OpenAI Assistants / Responses API Agent

适用于自建 OpenAI Agent、RAG Agent 或企业内部助手。

推荐部署方式：

1. 解压 `perovskite-tandem-research.zip`。
2. 将 `SKILL.md` 内容放入 Agent 的 system/developer instructions。
3. 将 `references/` 文件导入向量库或文件检索系统。
4. 将 `README_CN.md` / `README_EN.md` 作为用户文档保留。
5. 为 Agent 配置 Web search 或外部检索工具，用于最新事实核查。
6. 在 Agent 工作流中加入规则：
   - 论文分析优先检索 `paper-review-template.md`、`metrics-glossary.md` 和 `stability-assessment.md`。
   - 路线评估优先检索 `technology-routes.md` 和 `route-evaluation-framework.md`。
   - 最新效率、公司动态和产业化状态必须调用 Web search。

建议测试问题：

```text
根据最近公开资料，判断 perovskite/silicon tandem 是否已经具备商业化条件，并给出证据等级。
```

### 4. Claude Projects

Claude Projects 不一定支持 ChatGPT Skill ZIP 的原生安装，但可以把该 Skill 作为 Project Knowledge 使用。

建议步骤：

1. 解压 `perovskite-tandem-research.zip`。
2. 创建一个 Claude Project。
3. 将 `SKILL.md` 放入 Project Instructions 或项目说明。
4. 上传 `references/` 文件作为 Project Knowledge。
5. 上传 `README_CN.md` / `README_EN.md` 作为说明文档。
6. 如果需要最新事实，确保使用带联网能力的 Claude 环境，或要求用户提供最新来源。

### 5. Gemini Gems

Gemini Gems 通常以自定义指令和知识文件形式使用。

建议步骤：

1. 解压 `perovskite-tandem-research.zip`。
2. 创建 Gem。
3. 将 `SKILL.md` 的核心规则写入 Gem Instructions。
4. 上传 `references/` 文件作为知识材料。
5. 如使用联网能力，要求 Gem 在涉及最新论文、效率纪录和公司动态时优先查证。

### 6. Cursor / Windsurf / Cline / Roo Code 等代码 Agent

这些工具更适合把 Skill 作为项目级 Agent 指令使用，而不是原生安装。

建议项目结构：

```text
project-root/
├── .agent/
│   └── perovskite-tandem-research/
│       ├── SKILL.md
│       ├── README_CN.md
│       ├── README_EN.md
│       └── references/
└── AGENTS.md 或 CLAUDE.md 或 .cursorrules
```

部署步骤：

1. 解压 `perovskite-tandem-research.zip` 到项目目录下的 `.agent/perovskite-tandem-research/`。
2. 在 `AGENTS.md`、`CLAUDE.md`、`.cursorrules` 或工具支持的规则文件中加入：

```text
When the task concerns perovskite solar cells, perovskite/silicon tandems, all-perovskite tandems, PV efficiency records, stability, scale-up, manufacturing, or photovoltaic R&D strategy, follow .agent/perovskite-tandem-research/SKILL.md and consult the references folder as needed.
```

3. 如工具支持浏览器或 MCP 搜索工具，启用联网检索。
4. 如果工具无联网能力，则只能进行框架化分析，不能声称已核查最新事实。

### 7. Dify / Coze / LangChain / LlamaIndex 等工作流 Agent

适用于构建 RAG 或多步骤研究助手。

建议部署方式：

1. 解压 `perovskite-tandem-research.zip`。
2. 将 `SKILL.md` 作为系统提示或应用说明。
3. 将 `references/` 文件导入知识库，并保持文件名作为 metadata。
4. 建议建立以下检索路由：
   - `paper-review`：检索 `paper-review-template.md`、`metrics-glossary.md`、`stability-assessment.md`。
   - `research-scan`：检索 `literature-map.md`、`key-papers.md`、`literature-update-rules.md`。
   - `route-evaluation`：检索 `technology-routes.md`、`route-evaluation-framework.md`。
   - `rd-decision`：检索 `rd-decision-framework.md`、`go-no-go-scorecard.md`。
   - `experiment-planning`：检索 `experiment-planning.md`、`stability-assessment.md`。
   - `competitor-watch`：检索 `competitor-watchlist.md`、`source-priority.md`，然后调用 Web search。
5. 为最新事实核查配置 Web search 节点，并要求输出来源。

### 8. 本地文件夹直接使用

如果只是希望手动使用该 Skill：

1. 解压 `perovskite-tandem-research.zip`。
2. 打开 `SKILL.md`，把核心规则复制给任意大模型。
3. 根据任务把相关 `references/` 文件一并提供给模型。
4. 涉及最新事实时，让模型联网查证或手动提供最新资料。

## 安装后验证清单

安装后建议依次测试：

```text
1. 帮我精读一篇钙钛矿/硅叠层论文。
2. 比较 2T 和 4T 钙钛矿/硅叠层路线。
3. 设计一个宽带隙钙钛矿顶电池的三个月实验计划。
4. 核查某家公司最新钙钛矿/硅叠层效率纪录。
5. 给出某条技术路线的 Go / Conditional Go / Watch / No-Go 判断。
```

正常结果应满足：

- 默认中文输出。
- 对最新事实主动要求或执行联网查证。
- 区分认证效率与自报效率。
- 区分小面积电池、minimodule 和商业组件。
- 对稳定性数据检查封装、MPP tracking、光强、温度、湿度和测试时长。
- 对研发决策输出 Go / Conditional Go / Watch / No-Go。

## 更新维护建议

- 每月更新 `key-papers.md` 和 `competitor-watchlist.md`。
- 每季度更新 `technology-routes.md`、`route-evaluation-framework.md` 和 `go-no-go-scorecard.md`。
- 每次出现新的认证效率纪录或重大公司进展时，更新 `literature-update-rules.md` 中的检索提示或新增文献卡片。
- 不建议把大量论文全文直接塞入 Skill；更推荐维护结构化论文卡片和动态检索规则。
