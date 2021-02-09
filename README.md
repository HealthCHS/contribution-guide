# 构建指南

首先欢迎大家加入到这里，欢迎大家帮助构建。

## 内容组成

目前我们的项目包含如下组成部分

- contribution-guide -> 构建手册
- NHS -> 翻译终了的 NHS 内容
- NHSConditionsSrc -> 这是用于存储 NHS Conditions 相关页面的原始内容

## NHS 存储库

这是用于存储翻译终了的 NHS 内容。

### 劳动标记

由于 NHS 是英国的区域性服务，出现区域性资料是必然发生的。如果发现区域性内容，请通过类似 ``<!-- FIXME: 潜在的区域性内容 -->`` 进行标记。
这将有助于后期我们公开资料时进行标注。

由于可能存在的多人交互操作，建议在选择好内容后在目录用 `[WIP]` 进行标记以防止多人重复劳动，当然这不是必须的。

例如：

```markdown
- [ ] [WIP] AAA
```

### 文件命名

请使用与 NHSConditionsSrc 存储库相同的文件命名。

### 工作流程

原则上工作流程应由 NHSConditionsSrc 完成单元搬运后进行翻译。

## NHSConditionsSrc 存储库

这是用于存储 NHS Conditions 相关页面的原始内容的存储库，原始内容可以由 <https://www.nhs.uk/conditions/> 进行获取。

### 文件命名

文件明明请参阅对应文档目录后缀。  
例如 `https://www.nhs.uk/conditions/zika/` 应该为 `zika.md` 而非 `Zika-virus.md` 或者其他。

如若文档存在分支，则使用 `-` 替代目录中的 `/`。  
例如 `https://www.nhs.uk/conditions/abdominal-aortic-aneurysm/treatment/` 中，`treatment` 为分支，文件名应该为 `abdominal-aortic-aneurysm-treatment.md`。

### 劳动标记

对于劳动标记请参阅 [NHS 存储库](#%E5%8A%B3%E5%8A%A8%E6%A0%87%E8%AE%B0)。

### 文件链接

当完成搬运请将对应条目链接到对应文档。此处应使用相对目录。

### 注意事项

以下内容不需要被包含

- 潜在的暂时更正（例如因疫情原因，对应的区域服务更正）

