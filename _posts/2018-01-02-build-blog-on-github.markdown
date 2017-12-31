---
layout: post
title: 在github上建立部落格
date: 2018-01-02 00:00:00.000000000 +08:00
tag: GitHub
---

### 基本建造

GitHub + jekyll + Vno（jekyll的主題）

#### Step 01/02 - 建立 GitHub Page
首先需先建立GitHub帳號：https://github.com/<br>
登入後GitHub後，右上加號圖示 -> New Repository<br>
Repository name 輸入 『你的用户名.github.io』，注意大小寫要同你的用戶名<br>
git clone 這個新建的 repository 到電腦裡<br>

隨便新增一個 index.html ， push 到 GitHub 上，<br>
接著在瀏覽器網址內輸入 『你的用户名.github.io』，確認是否已可建立。<br>

#### Step 02/02 - 使用jekyll + Vno主題

確認後，git clone https://github.com/onevcat/vno-jekyll.git<br>
或者直接下載zip後解壓縮到資料夾<br>

cd 到該資料夾內 bundler install<br>
接著下 bundler exec jekyll serve --watch 就可在 localhost:4000 看到建立的部落格<br>

### 開始使用

#### 初設置

在 _config.yml 檔案中可以更改基本資料及設置<br>
例如：cover_color佈景主要色彩等<br>
如要更換大頭貼或背景則在 assets/images 的資料夾內取代原本的 background 或 avatar(大頭照)<br>

#### 設置留言

到<a href="https://disqus.com/" target="_blank">disqus</a>申請帳號<br>
登入後在首頁點選 get started -> I want to install Disqus on my site -> 填寫資料<br>
記住填寫的 Website name，打開_config.yml，<br>
找到comment下的 disqus，將冒號後的資料改成剛剛的 Website name<br>

#### 新增文章

在 _posts資料夾內新增 yyyy-mm-dd-名字.markdown，markdown檔案內的最上方加入以下訊息(記得自行修改)：
```bash
---
layout: post
title: 文章標題
date: 2018-01-02 00:00:00.000000000 +08:00
tag: GitHub
---
```

下方就可以直接隨意開始寫文章了，檔案會在 _site/yyyy/mm 自動生成
