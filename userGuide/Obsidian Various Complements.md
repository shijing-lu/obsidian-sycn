# Obsidian Various Complements 插件完全指南

> Various Complements 是 Obsidian 中功能最强大的自动补全插件，支持从当前文件、整个库、自定义词典、内部链接、Front matter 等多个来源提供补全建议。

---
technology
## 一、插件简介

Various Complements 的核心功能是在你输入文字时，**智能弹出补全候选词**，来源涵盖：

- 当前文件中出现过的词
- 整个 Obsidian 库中的词汇
- 自定义词典文件（配合 Language Learner 等插件使用）
- 库中的内部链接（笔记标题、别名）
- Front matter 中的字段值

---

## 二、全局设置（Filter Settings）

这些设置影响所有补全来源的整体行为。

### 匹配策略

|选项|说明|
|---|---|
|**Strategy**| `default`：标准匹配；`greedy`：贪婪模式，更激进地匹配候选词|
|**Fuzzy match**|开启后允许模糊匹配，输入 `prd` 也能匹配 `president` |
|**Min full match chars**|触发全词精确匹配所需的最少字符数|

### 字符处理

|选项|说明|
|---|---|
|**Treat accent distinctions as alphabetic characters**|将带重音的字母（如 é、ü）视为独立字母处理，适合学习法语、德语等|
|**Treat `_` as a part of a word**|将下划线视为单词的一部分，适合编程场景中的变量名补全|
|**Probably extinct docs**|忽略长期未修改的"过时"笔记，提升补全性能|

### 候选词数量控制

|选项|说明|
|---|---|
|**Max number of suggestions**|补全列表最多显示多少个候选项|
|**Max number of words as a phrase**|单个补全候选最多包含几个单词（用于短语补全）|
|**Min number of characters for trigger**|输入至少几个字符后才触发补全，避免过早弹出|

### 补全行为

|选项|说明|
|---|---|
|**Complement automatically**|开启后自动弹出补全列表，无需手动触发|
|**Select with seconds for trigger**|设置自动选中第一个候选的延迟秒数，0 表示不自动选中|
|**Disable suggestions in the Math block**|在数学公式块（`$...$`）内禁用补全，避免干扰公式输入|
|**Disable suggestions in the Code block**|在代码块内禁用补全|
|**Insert code after completion**|补全后在词尾自动插入指定字符（如空格或标点）|

### 触发抑制

|选项|说明|
|---|---|
|**First characters to disable suggestions**|以指定字符开头时不触发补全（如输入 `/` 或 `#` 时）|
|**Use patterns to suppress trigger**|开启正则模式，根据上下文判断是否触发补全|
|**Phrase patterns to suppress trigger**|配置具体的正则表达式，匹配时压制补全弹出|
|**No auto focus until the cyclic**|循环候选前不自动聚焦补全列表，需手动按 Tab/Enter 选中|

---

## 三、快捷键（Hotkeys）

插件提供了一套完整的键盘操作方案：

|快捷键|作用|
|---|---|
| `Enter` |确认选中当前候选词|
| `Tab` |同上，确认补全|
| `↑` / `↓` |在候选列表中上下移动|
| `select 1st` ~ `select 9th` |直接选中列表中第 N 个候选|
| `navigation` |在候选之间导航|
| `Insert as text` |以纯文本形式插入（不触发链接等特殊格式）|

> 所有快捷键可在 Obsidian「设置 → 快捷键」中自定义修改。

---

## 四、当前文件补全（Current File Complement）

从**当前正在编辑的笔记**中提取词汇作为补全来源。

|设置项|说明|
|---|---|
|**Enable Current file complement**|开启/关闭本来源|
|**Min number of characters for indexing**|索引单词的最少字符数，过短的词（如 "a"、"is"）不纳入候选|
|**Only complement English or current file complement**|只补全英文词汇或仅限当前文件来源|
|**Max number of characters for indexing**|超过该长度的词不纳入索引|
|**Exclude word patterns for indexing**|通过正则排除不需要索引的词（如数字、特殊格式）|

**适用场景：** 在长文中重复使用相同术语时，非常实用。

---

## 五、当前库补全（Current Vault Complement）

从**整个 Obsidian 库**的所有笔记中提取词汇。

|设置项|说明|
|---|---|
|**Enable Current vault complement**|开启/关闭本来源|

> ⚠️ 库较大时开启可能影响性能，建议配合「Probably extinct docs」过滤旧文件。

---

## 六、自定义词典补全（Custom Dictionary Complement）

从**自定义 `.md` 词典文件**中读取补全候选，是与 Language Learner 插件联动的核心功能。

|设置项|说明|
|---|---|
|**Enable Custom dictionary complement**|开启/关闭本来源|
|**Custom dictionary paths**|填写词库笔记的路径，如 `LingQ/words_database.md` |
|**Column delimiter**|词库文件的分隔符，联动 Language Learner 时需改为 **Comma（逗号）**|

**配合 Language Learner 的配置流程：**

1. 将 Column delimiter 改为 **Comma**
2. 填写与 Language Learner 相同的词库路径
3. 执行 Language Learner「刷新单词数据库」命令
4. 执行「Reload custom dictionaries」刷新缓存
5. 写作时即可获得英↔中双向补全提示

---

## 七、内部链接补全（Internal Link Complement）

将库中**所有笔记的标题和别名**作为补全来源，输入时可直接插入 `[[链接]]`。

|设置项|说明|
|---|---|
|**Enable Internal link complement**|开启/关闭本来源|
|**Suggest with @ alias**|输入 `@` 时触发别名补全|
|**Preserve input letter case**|保留你输入时的大小写，不强制转换为笔记标题的大小写|
|**Enable internal links in new format**|使用新格式的内部链接|
|**Rotate with internal links**|候选列表循环时包含内部链接|
|**Insert nothing in this internal blank**|在内部链接的空白处不插入任何内容|
|**Invert oracle path**|反转路径预测逻辑|
|**Include prefix glob patterns**|用 glob 表达式过滤只包含特定前缀路径的笔记|
|**Front matter key for exclusion**|指定 Front matter 字段，含该字段的笔记不出现在补全中|
|**Tags for exclusion**|含指定 tag 的笔记不出现在内部链接补全中|
|**Min number of characters for trigger**|触发内部链接补全的最少输入字符数|

**适用场景：** 快速插入笔记链接，构建知识网络。

---

## 八、Front Matter 补全（Front Matter Complement）

当光标在笔记的 **Front matter** 区域内时，自动补全字段值（如 tags、status 等已使用过的值）。

|设置项|说明|
|---|---|
|**Enable Front matter complement**|开启/关闭本来源|

**适用场景：** 统一管理笔记的 tag 和属性值，避免拼写不一致。

---

## 九、智能排序（Intelligent Suggestion Prioritization）

根据**历史选择记录**，将你更常选择的候选词排在前面。

|设置项|说明|
|---|---|
|**Enable Intelligent suggestion Prioritization**|开启/关闭智能排序|
|**History file grow**|历史记录文件的增长策略|
|**Max word to keep history**|最多记录多少个词的历史选择|
|**Max number of histories to keep**|每个词最多保留多少条历史记录|

> 开启后插件会学习你的使用习惯，越用越准。

---

## 十、移动端与调试

|设置项|说明|
|---|---|
|**Disable on mobile**|在手机端禁用插件（移动端性能有限，建议开启）|
|**Show log about performance in a console**|在开发者控制台输出性能日志，用于排查卡顿问题|

---

## 十一、推荐配置组合

### 英语学习场景（配合 Language Learner）

```
Strategy: default
Fuzzy match: 开启
Min number of characters for trigger: 2
Complement automatically: 开启
Disable suggestions in the Math block: 开启
Disable suggestions in the Code block: 开启
Custom dictionary complement: 开启
Column delimiter: Comma
Custom dictionary paths: LingQ/words_database.md
Intelligent Suggestion Prioritization: 开启
```

### 中文笔记写作场景

```
Strategy: greedy
Current vault complement: 开启
Internal link complement: 开启
Front matter complement: 开启
Min number of characters for trigger: 1
Suggest with @ alias: 开启
Intelligent Suggestion Prioritization: 开启
```

### 轻量模式（性能优先）

```
Current vault complement: 关闭
Probably extinct docs: 开启
Max number of suggestions: 5
Disable on mobile: 开启
```

---

## 十二、常用快捷操作速查

|操作|方法|
|---|---|
|手动触发补全|默认可在设置中绑定快捷键|
|刷新自定义词典|命令面板 → `Reload custom dictionaries` |
|确认补全| `Enter` 或 `Tab` |
|取消补全| `Esc` |
|直接选第 N 个候选|绑定 `select Nth` 快捷键|

---

_插件作者：tadashi-aikawa | 适用版本：Various Complements 最新版_