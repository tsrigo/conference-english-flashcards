# Academic Conference English Flashcards

一个单文件网页，用来练习国际学术会议常见英语表达：自我介绍、研究速讲、海报交流、提问、回答与救场、听力救场、口头报告和社交联系。

数据只保存在浏览器本地。大批量修改卡片前，建议先在页面顶部点击“导出数据”备份 JSON；修改完成后再用“导入数据”导回页面。

可以把导出的 JSON 发给 LLM，并使用这个 prompt：

```text
请帮我修改这份学术会议英语记忆卡 JSON。

要求：
1. 只修改 cards 数组里的卡片内容，不改变 JSON 顶层结构。
2. 保留每张卡片的字段：id、category、type、front、answer、note、tags、due、interval、ease、reps、lapses、created。
3. 可以新增、删除或改写卡片，但 id 必须唯一。
4. front 写中文题面或场景，answer 写自然、简洁的英文表达，note 写中文使用提示。
5. 最终只返回可直接导入的 JSON，不要额外解释。
```
