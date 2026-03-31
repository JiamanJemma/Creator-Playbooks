# 视频处理 Playbook

## 下载

| 触发 | 命令 |
|------|------|
| 下载视频 | `yt-dlp -f "bestvideo[height<=1080]+bestaudio" --merge-output-format mp4 -o "~/outputs/videos/%(title)s.%(ext)s" <URL>` |
| 下载播放列表 | 同上 + `-o "~/outputs/videos/%(playlist_index)s-%(title)s.%(ext)s"` |
| 下载MP3 | `yt-dlp -x --audio-format mp3 --audio-quality 0 -o "~/outputs/audio/%(title)s.%(ext)s" <URL>` |

下载失败时加：`--cookies-from-browser safari`

## 剪辑

| 触发 | 命令 |
|------|------|
| 剪辑/从X到Y | `ffmpeg -i <INPUT> -ss <START> -to <END> -c copy ~/outputs/videos/<OUTPUT>` |
| 压缩视频 | `ffmpeg -i <INPUT> -vcodec libx264 -crf 28 -preset medium -acodec aac -b:a 128k ~/outputs/videos/<OUTPUT>` |
| 合并视频 | concat_list.txt → `ffmpeg -f concat -safe 0 -i concat_list.txt -c copy ~/outputs/videos/<OUTPUT>` |
| 转竖屏 | `ffmpeg -i <INPUT> -vf "split[original][blur];[blur]scale=1080:1920:force_original_aspect_ratio=increase,crop=1080:1920,boxblur=25[bg];[original]scale=1080:-1[fg];[bg][fg]overlay=(W-w)/2:(H-h)/2" -c:a copy ~/outputs/videos/<OUTPUT>` |

## 字幕

| 触发 | 命令 |
|------|------|
| 生成字幕 | `whisper <FILE> --model medium --language zh --output_format srt --output_dir ~/outputs/subtitles` |
| 优化字幕 | `cat <SRT> \| gemini -p "优化字幕，修正错别字，保持原意" > ~/outputs/subtitles/<OUTPUT>` |
| 筛选片段 | 读取字幕 → 表格展示 → 佳蔓选 → 批量剪辑 |

### 字幕格式偏好
- **每条字幕只显示一行**，不要两行叠在一起
- **每行最多 13 个字**，超过的要断句拆开
- 断句时按语义自然停顿拆分，不要把一个词拆开
