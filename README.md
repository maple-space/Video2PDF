# Video2PDF

适合将任何线上影片、课程压制成一桢一桢播放的PDF

## pre-Installation

需要先安装 `moviepy`
```
pip install moviepy
```

### 执行
#### 功能 1. 压制
`python main.py xxx.mp4`

* 需要两个档案 mp4, srt （不管有没有内嵌字幕档，都需要 srt 当时间参考点）
* srt 必须是 `xxx.zh.srt`
* 将同名的 mp4 与同名的 srt 放在一起，执行 `python main.py xxx.mp4` 等待一定时间即会产生 pdf
* 如果影片已经有预设 srt 不需 srt 压制进去只需要档参考点，请用 `python main.py xxx.mp4 --embed`

#### 功能 2. 下载 Youtube 影片并下载字幕、翻译

`python you_dt.py [youtube_url]`

#### 功能 3. 纯翻译字幕

`python translate_srt.py xxxx.srt`



### 注意事项

* 档案太大会遇到同时开启个数限制
* 先执行 `ulimit -n 4096` 可以解决

### 不喜欢指定字体可以换

执行 `python font.py` 察看你有哪些 font 可以用

### 推荐工具

* 下载工具：yt-dlp
* 下载字幕工具：YouTube™ 双字幕 https://chrome.google.com/webstore/detail/youtube-dual-subtitles/hkbdddpiemdeibjoknnofflfgbgnebcm?hl=zh-TW
* 听译字幕工具：https://goodsnooze.gumroad.com/l/macwhisper
* 翻译字幕工具：https://translatesubtitles.co/


### TODO

- [x] 双语字幕
- [x] 多核 CPU 平行处理
- [ ] Streamlit UI 介面
- [ ] 向量检索
- [ ] PDF searchable
