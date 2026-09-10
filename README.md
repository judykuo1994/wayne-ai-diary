# Wayne 的 AI 日記

喬大地產週會分享用的簡報，24 頁。

網址：<https://judykuo1994.github.io/wayne-ai-diary/>

## 這個 repo 只放成品

`index.html` 是**產生出來的**，不要直接編輯。原始碼、素材與製作說明在另一個 private repo
`judykuo1994/wayne-ai-diary-deck`（本機工作區 `~/Desktop/Wayne AI日記/`）。

改版流程：

```bash
cd ~/Desktop/Wayne\ AI日記
# 1. 改 03-簡報/wayne-ai-diary.src.html
/usr/bin/python3 04-腳本/build.py 03-簡報/wayne-ai-diary.src.html \
    03-簡報/wayne-ai-diary.html 03-簡報/assets.json .
# 2. 重出這個 repo 的 index.html
04-腳本/build_pages.sh ~/Desktop/wayne-ai-diary-web/index.html
# 3. push
cd ~/Desktop/wayne-ai-diary-web && git add -A && git commit -m "..." && git push
```

## noindex

頁面掛了 `<meta name="robots" content="noindex,...">`，另有 `robots.txt` 擋爬蟲。
拿到網址的人看得到，但不希望被搜尋引擎收錄——內容含去識別化過的客戶文件影像。
