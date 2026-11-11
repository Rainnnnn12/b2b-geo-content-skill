# B2B GEO Content Skill

用于 B2B GEO（Generative Engine Optimization，生成式引擎优化）内容策划、研究、写作和审核的 AI Skill。

技能名称：`write-b2b-geo-content`  
显示名称：B2B GEO内容撰写

## 工作流程

围绕已确认的 B2B Prompt，完成单篇文章生产：

1. **初始输入**：确认 Prompt、目标受众（TA）、用户所处阶段，以及相关客户资料。
2. **选题**：拆解问题、轻量检索，提出并评分 3 个候选选题，等待用户确认。
3. **大纲生成**：规划标题、结构、证据、产品承接、FAQ 和参考资料，等待用户确认。
4. **终稿生成**：按已确认大纲写作，核查客户事实、引用和内容完整性，输出正文及内部检查结果。

适用于 Prompt Library 之后的单篇 GEO 文章生产；不包含 Prompt 生成、内容发布或可见度监测。

## 使用前准备

- 一个已确认的 B2B Prompt。
- 对应目标受众，以及意识、考虑或决策阶段。
- 可用的客户业务、产品、案例及内容策略资料。
- 需要核验外部来源时，可用的网页检索能力。

## 使用方式

下载或克隆本仓库，将 `write-b2b-geo-content/` 整个目录导入所用 AI 工具的 Skill 管理功能，或放入该工具支持的技能目录。具体导入方式以所用工具为准。

安装时保留 `SKILL.md`、`agents/`、`assets/` 和 `references/` 的相对位置。

可使用以下提示开始：

```text
使用 $write-b2b-geo-content 根据以下信息完成一篇 B2B GEO 文章：

Prompt：[填写用户问题]
TA：[填写目标受众]
阶段：[意识 / 考虑 / 决策]
客户资料：[提供相关资料或可访问的位置]

从初始信息确认开始，按 Skill 的阶段推进。
```

## 文件结构

```text
write-b2b-geo-content/
├── SKILL.md
├── agents/
│   └── openai.yaml
├── assets/
│   └── icon.svg
└── references/
    ├── article-structure-templates.md
    ├── article-writing-rules.md
    ├── audit-table-template.md
    ├── disclaimer-template.md
    ├── source-research-rules.md
    └── topic-selection-rules.md
```

`SKILL.md` 定义主流程；参考文档提供选题、文章结构、写作、资料研究、内部检查及免责声明模板。
