# Academic Conference English Flashcards

一个单文件网页，用来练习国际学术会议常见英语表达：自我介绍、研究速讲、海报交流、提问、回答与救场、听力救场、口头报告和社交联系。

数据只保存在浏览器本地。大批量修改卡片前，建议先在页面顶部点击“导出数据”备份 JSON；修改完成后再用“导入数据”导回页面。

可以把导出的 JSON 发给 LLM，并使用这个 prompt。先填写个人信息，再把导出的 JSON 粘到最后：

```text
请帮我修改这份学术会议英语记忆卡 JSON。

我的个人信息：
- 姓名：
- 机构/学校：
- 身份：例如 PhD student / master student / researcher
- 研究领域：
- 具体研究问题：
- 论文/项目标题：
- 方法或系统名称：
- 使用的数据/方法：
- 主要目标：
- 主要贡献：
- 初步结果：
- 主要限制：
- 下一步计划：
- 会议名称：
- 展示形式：poster / oral talk / workshop presentation / 其他
- 论文或项目链接：
- 联系方式：email / LinkedIn / 个人主页
- 其他希望加入卡片的信息：

要求：
1. 根据上面的个人信息，替换卡片里的 [姓名]、[机构]、[研究领域]、[具体问题]、[主题]、[方法]、[目标]、[贡献]、[限制]、[计划] 等空位。
2. 如果某项个人信息为空，就保留对应方括号占位，不要编造。
3. 只修改 cards 数组里的卡片内容，不改变 JSON 顶层结构。
4. 保留每张卡片的字段：id、category、type、front、answer、note、tags、due、interval、ease、reps、lapses、created。
5. 可以新增、删除或改写卡片，但 id 必须唯一。
6. front 写中文题面或场景，answer 写自然、简洁的英文表达，note 写中文使用提示。
7. 最终只返回可直接导入的 JSON，不要额外解释。

导出的 JSON：
{在这里粘贴从网页导出的 JSON}
```
