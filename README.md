# 构建指南

首先欢迎大家来到到这里，同样欢迎大家帮助构建。  
大家可以通过 PR 的方式帮助我们进行。  
或者电邮我 [realkevin@tutanota.com](mailto:realkevin@tutanota.com) 来加入组织。



## 内容组成

目前我们的项目包含如下组成部分

- contribution-guide -> 构建手册
- NHS -> 翻译终了的 NHS 内容
- NHSConditionsSrc -> 这是用于存储 NHS Conditions 相关页面的原始内容



## NHS 存储库

这是用于存储翻译终了的 NHS 内容。

### 劳动标识

由于暂时缺失索引，所以可行的劳动标记方案只能是在文档尾部增添 WIP 标记。

例如你想翻译 NHSConditionsSrc 的 AAA.md 文档但是又暂时翻译不完或者只想占着，那么你需要创建 AAA.md 并包含 WIP 标记并提交到存储库。

可参考的 WIP 标记可以是：

- `Work in progress by xxxx`
- `WIP by xxx`
- etc.

希望能够在 WIP 标记中添加你的名字以方便联络。当然，这是可选项。

### 文件命名

请使用与 NHSConditionsSrc 存储库相同的文件命名。

### 工作流程

原则上工作流程应由 NHSConditionsSrc 完成单元搬运后进行翻译。

### 注意事项

- 请避免主观化语言！



## NHSConditionsSrc 存储库

这是用于存储 NHS Conditions 相关页面的原始内容的存储库，原始内容可以由 <https://www.nhs.uk/conditions/> 进行获取。

### 文件命名

文件明明请参阅对应文档目录后缀。  
例如 `https://www.nhs.uk/conditions/zika/` 应该为 `zika.md` 而非 `Zika-virus.md` 或者其他。

如若文档存在分支，则使用 `-` 替代目录中的 `/`。  
例如 `https://www.nhs.uk/conditions/abdominal-aortic-aneurysm/treatment/` 中，`treatment` 为分支，文件名应该为 `abdominal-aortic-aneurysm-treatment.md`。

### 劳动标识

由于 NHS 是英国的区域性服务，出现区域性资料是必然发生的。如果发现区域性内容，请通过类似 ``<!-- FIXME: 潜在的区域性内容 -->`` 进行标记。
这将有助于后期我们公开资料时进行标注。

由于可能存在的多人交互操作，建议在选择好内容后在目录用 `[WIP:用户名]` 进行标记以防止多人重复劳动，当然这不是必须的。

例如你的用户名为 KZ，你想占坑 AAA，那么正确的标识方法应该为：

```markdown
- [ ] [WIP:KZ] AAA
```

其中用户名是你的用户名。

我们推荐你加入用户名是因为能够更好的沟通。当然，这是可选项。


### 文件链接

当完成搬运请将对应条目链接到对应文档。此处应使用相对目录。

### 注意事项

以下内容不需要被包含

- 潜在的暂时更正（例如因疫情原因，对应的区域服务更正）

### Markdown 格式规范

1. 在文档开头，请注释指向的目录。  
例如 <https://github.com/NHSZH/NHS/blob/master/abdominal-aortic-aneurysm.md>  
文件 `abdominal-aortic-aneurysm.md` 指向 `AAA` 与 `Abdominal aortic aneurysm`，使用请使用注释 `<!-- AAA/Abdominal aortic aneurysm -->`  
这将有助于以后的构建。

2. 文章的二级标题（`##`）前请增加三行空行以便于分割段落。  
列如
```markdown
xxxx
<!-- 第一行，注释请勿输入 -->
<!-- 第二行，注释请勿输入 -->
<!-- 第三行，注释请勿输入 -->
## ...
```
这将提升文件可读性。

3. 对于文章的结尾标记，请使用类似如下格式：
```markdown
***Page last reviewed: 12 January 2021  
Next review due: 12 January 2024***
```  
当然，如果你想加入你的搬运名称可以使用如下格式：
```markdown
***Page last reviewed: 12 January 2021  
Next review due: 12 January 2024  
Mover： xxxx***
```  
或者
```markdown
***Page last reviewed: 12 January 2021  
Next review due: 12 January 2024  
Mover： xxxx  
Mover Date: 14 January 2021***
```  
这个很重要，以后可能存在的定期文档更新，CI 可能需要合理的格式。
