# 考研408 Skills (`kaoyan-408`)

把考研四科（数学一 / 英语一 / 政治 / 408）讲次材料写入 Obsidian 知识库。

## 安装

```bash
npx skills add PioneerSunOvO/skills-kaoyan-408
# 或克隆到本机 skills 目录，文件夹名为 kaoyan-408
```

Cursor / Claude：内容放在 `skills/kaoyan-408/`（与 `name: kaoyan-408` 一致）。

## 触发（一句）

```
使用考研408 Skills 将我提供的资料写入知识库。
材料：
```

下一行附材料路径即可。库规由 skill 自动读取（`00-系统/`）。

## 默认行为

1. Phase1 → `人工智能初稿/`
2. Phase2 → 正式教材夹（同轮；不覆盖已校对正文）
3. 中间产物 → `tmp/`（相对 vault 根）
4. 视频仅可放各科 `资料/`

Vault 根以当前打开的知识库为准，不写死绝对路径。

## 文件

| 文件 | 说明 |
|------|------|
| SKILL.md | 主流程 |
| templates.md | 笔记骨架 |
| media-pipeline.md | OCR / Whisper |
| subject-routing.md | 四科分流 |
| examples.md | 样板 |
| quality-rules.md | 质量自检 |

## License

MIT
