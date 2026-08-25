# Absorbed rules（借鉴规则 · 已适配本库）

来源： [Treasoni/kaoyan_skills](https://github.com/Treasoni/kaoyan_skills) 等公开 skill；**不安装整仓**，只吸收可复用规则。

## 1. 章节完整性（来自 chapter-summary）

Phase2 收尾前对照（数学/408）：

```
□ 书中「方法总结 / 重要结论 / 公式」框是否进速查卡？
□ 考情、重难点是否在章总览？
□ 有视频则口播独有点是否进补遗或分笔记？
□ 分笔记是否可从 MOC 一跳到达？
□ OCR 乱码处是否标「待人工核对」而非大段粘贴？
```

政治/英语：

```
□ 一章一文件是否含「本章小结」？
□ 背诵/易混是否单独列出？
```

## 2. 已有笔记保护（来自 kaoyan-math-notes）

- 写前检查目标路径是否已有文件
- **不覆盖**已有人工填写正文
- 只为缺失文件建骨架；汇报「已存在 / 新建」清单
- 增量更新用注释或新小节，不删原段

## 3. 理解校验（来自 understanding）

人工智能初稿必须保留：

```markdown
## 我的校对
### 我真正记住的
### 仍不懂、下次要盯的
```

正式分笔记（数学/408）留空位：

```markdown
## 一句话费曼
> 合上笔记，用自己的话讲清本小节。
```

用户要求「检查理解」时：核对推理链，指出跳步/概念混淆，**不替用户填「我的校对」**。

## 4. 错题归档（来自 mistake-book）

- 错题进 `错题/`，`parent` 双链回章总览
- 按**知识点模块**归档，不按题号表象堆
- 记错因 + 堵点关键词，不抄全解过程

## 5. 组织与安全（来自 knowledge-base-organizer）

- 大改目录/MOC 前先列出拟改清单
- 不破坏现有四层导航（首页 → 科目 → 课程 → 章）
- 知识缺口仅基于**已有笔记**推断，不臆造整章大纲

## 6. 本库明确不吸收

| 来源能力 | 原因 |
|----------|------|
| MemOS / sync | 无此外部记忆系统 |
| kaoyan-english-vocab / SM-2 | 单词不进库 |
| kaoyan-electronics / 822 | 非 408 初试科目 |
| opencli / mcp-builder 等 L3 工具 | 与讲次知识化无关，避免误触发 |
| 整仓 50+ skill 安装 | 维护成本与库规冲突 |

## 7. 可继续自研的伴生 skill（未安装，按需）

| 名称 | 用途 | 仓库路径 |
|------|------|----------|
| understanding | 推导/理解校验 | [understanding](https://github.com/Treasoni/kaoyan_skills/tree/main/understanding) |
| mistake-book | 错题快速归档 | [mistake-book](https://github.com/Treasoni/kaoyan_skills/tree/main/mistake-book) |
| chapter-summary | 已有笔记汇总成章节总结 | [chapter-summary](https://github.com/Treasoni/kaoyan_skills/tree/main/chapter-summary) |

完整外链清单见桌面：`D:\System\Program Files\Desktop\Atrust\考研知识库-可借鉴Skills.md`

本 skill 远程仓库：https://github.com/PioneerSunOvO/skills-kaoyan-408
本机目录：`~/.agents/skills/kaoyan-408/`（`.claude` / `.cursor` 为符号链接）

