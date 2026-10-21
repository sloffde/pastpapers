# 贡献指南 · 历年题站（pastpapers）

感谢你为 SLOFFDE 整理历年题！本仓库用 [Ginkgo](https://github.com/YangShu233-Snow/Ginkgo) 构建交互式题目站。

## 加一份新试卷

1. 把原始试卷转成 Ginkgo Markdown：在本地装 `pip install ginkgo-flashcards`，运行 `ginkgo prompt --memory`（已是 Markdown）或 `ginkgo prompt --standard`（其他格式）获取转换提示词，喂给 LLM 转换。
2. **脱敏**：抹除老师名、医院名、考生姓名学号班级；作者字段写脱敏署名。
3. 命名：放 `docs/<年级>/<科目>/<学年>-<学期>-<类型>.md`，如 `docs/大一/系统解剖学/2023-2024-期末.md`。
4. 格式参考：`docs/大一/系统解剖学/2023-2024-期末.md`（格式样例）。
5. 在 `ginkgo.yaml` 的 `nav` 里登记该文件。
6. 提 PR；合并后 GitHub Actions 自动构建上线。

## 格式速记

- front matter：`title` / `author` / `description`
- `## mcqs` 选择题：正确选项加 `[x]`，单/多选自动识别
- `## flashcards` 问答卡：一级列表=题干，二级列表=答案
- 题目之间用 `---` 分隔；报错就"大胆加缩进"

## 贡献方式（按门槛）

- 零基础：开 Issue 贴题目内容，维护者代为整理。
- 会网页：在 GitHub 网页端直接编辑 `.md` 提交。
- 标准：fork → 改 → PR。
