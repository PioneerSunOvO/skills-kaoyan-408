# Media pipeline（多格式摄入）

中间产物根（相对 vault 根）：**`tmp/`**  
例：`tmp/math-gaoshu-lec01_ocr/`

不写进正式笔记夹；不默认 git add `tmp/`。

## 0. 探测材料

1. 列出扩展名与体量
2. 已有合格产物（如 `tmp/{slug}_transcripts/v01.txt` 足够长）→ **跳过**重复转写
3. 若用户提供既有转写/OCR 路径 → **优先复用**，并在笔记 `source` 中注明；新产物仍写 `tmp/`

## 1. PDF

- **有文本层：** pdfplumber / PyMuPDF → `tmp/{slug}_pdf/`
- **扫描件：** 渲染 PNG → OCR → `tmp/{slug}_ocr/_all.txt`
- 框关键词：`方法总结`、`重要结论`、`公式`

## 2. 视频 / 音频

### 入库（允许）

| 允许 | 禁止 |
|------|------|
| `{科目}/资料/**` 或 `{课程}/资料/**` | 教材正式夹、`人工智能初稿/`、库根 |

用户视频已在 `资料/` → 原地引用；库外视频 → Phase1 清单建议相对路径后再移动。

### 转写（中间产物）

```
ffmpeg -i 资料/.../video.mp4 -vn -acodec libmp3lame -q:a 4 tmp/{slug}_audio/v01.mp3
# Whisper → tmp/{slug}_transcripts/v01.txt
```

多段视频按文件名 `v01…vN` 排序；进度写入口播补遗。

## 3. PPT / 图片 / 文档

| 格式 | 输出 |
|------|------|
| pptx | `tmp/{slug}_pptx/slides.txt` |
| png/jpg | `tmp/{slug}_img_ocr/` |
| md/txt/docx | 直接读或抽文本 |

## 4. 失败降级

| 情况 | 动作 |
|------|------|
| 无 ffmpeg | 提示安装；不假装已转写 |
| Whisper OOM | 降级 small 或分段 |
| OCR 乱码 | 标「待人工核对」；保留原图相对路径 |
| 格式不支持 | 汇报阻塞，请用户转换 |

## 5. 目录命名

```
tmp/
  {slug}_preview/
  {slug}_ocr/
  {slug}_audio/
  {slug}_transcripts/
  {slug}_pptx/
```

`slug` 例：`math-gaoshu-lec01`、`cs-ds-ch03`。
