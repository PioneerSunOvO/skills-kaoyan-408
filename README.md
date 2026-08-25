# 考研408 Skills (`kaoyan-408`)

把考研四科（数学一 / 英语一 / 政治 / 408）讲次材料写入 Obsidian 知识库。

## 安装

```bash
npx skills add PioneerSunOvO/skills-kaoyan-408
# 或克隆到 skills 目录：
# git clone https://github.com/PioneerSunOvO/skills-kaoyan-408.git ~/.agents/skills/kaoyan-408
```

Cursor / Claude：将本仓库内容放到 `skills/kaoyan-408/`（目录名与 `name: kaoyan-408` 一致）。

## 触发（一句）

```
使用考研408 Skills 将我提供的资料写入知识库。
材料：
```

下一行附 PDF / 视频 / 转写路径即可。库规由 skill 自动读取。

## 默认行为

1. Phase1 → `人工智能初稿/`
2. Phase2 → 正式教材夹（同轮；不覆盖已校对正文）
3. 中间产物 → `{vault}/tmp/`
4. 视频仅可放各科 `资料/`

默认 vault：`D:\Develop\Project\408`（可覆盖）。

## 文件

| 文件 | 说明 |
|------|------|
| SKILL.md | 主流程 |
| templates.md | 笔记骨架 |
| media-pipeline.md | OCR / Whisper |
| subject-routing.md | 四科分流 |
| examples.md | 样板 |
| absorbed-rules.md | 借鉴规则 |

## License

MIT
