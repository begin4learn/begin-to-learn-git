### Git Beginner

| git Command | Explain | syntax | Note |
| :--- | :--- | :--- | :--- |
| git--version | 確認是否安裝成功 |  |  |
| git config --global user.name"user name" | 告訴Git使用者資訊 | git config --global user.name"Lynn19931205" |  |
| git config --global user.email"email address" | 告訴Git使用者資訊 | git config --global user.email"j890355b@gmail.com" |  |
| git config --list | 看你的Git設定內容 |  |  |
| cd ~/desktop$ | 至桌面 | cd~/desktop$mkdir project\_1 |  |
| mkdir project\_1 | 創建一個叫做project\_2的資料夾 |  |  |
| cd ~/desktop/project\_1/ |  | cd~/desktop/project\_1/ |  |
| touch hello.txt | 創建一個名稱為hello.txt的文件 | touch hello.txt |  |
| git clone | clone下來別人的專案到local端 | gitclone [https://github.com/sarcadass/granim⋯⋯New\_Project](https://github.com/sarcadass/granim⋯⋯New_Project) |  |
| git init | 創建一個新的Repository\(打開任何一個專案資料夾打上git init\) |  |  |
| ls -ls | 列出專案資料夾下的檔案和資料夾 | ls -la | -l 列出詳細資料 -a 為列出隱藏資料夾 |
| git status | 查看目前的Git狀態:「hello.txt」這個檔案還沒有被追蹤 |  | Untracked files: 有新增新的檔案，但是還沒進到 git 追蹤範圍中/暫存區 |
| git add主檔名.副檔名 | 將檔案提交入Staging Area | git add主檔名.副檔名 |  |
| git status | 顯示目前工作環境狀態 | git status | On branch master |
| git add | 將整個資料夾的檔案都一起推送上去到Staging Area | git add不輸入檔案名稱 | 進入暫存區\(ADD\) |
| git commit -m '一行解說文字' | 將Staging Area內的東西推到Repository成為正式的版本 | git commit -m 'Add a line' | 提交版本\(COMMIT\) |
| git status | 查看目前狀: 工作區很乾淨噢，沒有新的修改、Staging Area裡面也沒有東西 |  | On branch master,               nothing to commit, working tree clean |
| git log | 查看所有的commit紀錄 |  | 查看目前狀 |
| git rm--cached | 將不在Repository的檔案移出Staging Area | git rm--cached hello.txt | 將檔案移出的暫存區 |
| git rm--cached | 檔案已經在repository內,從repository刪除，並且從stage刪除，檔案會從tracked變成untracked |  | 將檔案移出的暫存區 |
| git rm--cached | 檔案不在repository內,移除Staing Area中的檔案 |  | 將檔案移出的暫存區 |
| git reset HEAD檔案名稱 | 將已經在Repository的檔案,移出Staging Area |  | 將檔案移出的暫存區 |
| git diff | 比較文件或commit間修改的差異 |  | 查看目前狀 |
| git diff commit代碼 | 比較兩次commit間修改的差異 | git diff 8a85090dc97a | 第一欄的 commit代碼 複製起來(複製六碼或以上)
 |
| git log | 查看所有的commit紀錄: commit 8a85094b22edf4184e7228c3f849807dd7eed2c9 |  | 查看目前狀 |
| git show | 查看某項特定commit的修改內容,詳細列出該次commit的修改內容 | git show 8a8509 | 第一欄的commit代碼複製起來\(複製六碼或以上\) |
| git status | 列出目前的檔案狀態 |  | 查看目前狀 |
| [打開 https://github.com/ 網站](https://l.facebook.com/l.php?u=https%3A%2F%2Fgithub.com%2F&h=ATP4pyBaH6lENbLvLZAk-sSNNu1wrO0HG9MxBGgjTpSL1_e0H9xpv3DVSVvKpXhvcRZ2R1BUc3lruNFY1OsXsc05BZu2DzJAoWL5-ZOTKchiqTpwX6qAsyeyv7glizoeMJGJtRKbqBy1&s=1) |  |  |  |
| 在GitHub上創建一個和本地端名稱相同的資料夾，專案描述可寫可不寫、權限設為開放、README不用勾選 |  |  |  |
| git remote add origin [https://github.com/Lynn19931205/project\_1.git](https://github.com/Lynn19931205/project_1.git) | 將Local端的程式碼推到GitHub網站 |  | repository已存在 |
| git push -u origin master | 將Local端的程式碼推到GitHub網站 |  | repository已存在 |
| git pull | 將程式碼從Remote端拉下來到Local端 |  |  |
| edit conflict |  |  |  |
| git add | 將整個資料夾的檔案都一起推送上去到Staging Area |  |  |
| git commit | 將Staging Area內的東西推到Repository成為正式的版本 |  |  |
| git push | push to GitHub,推送程式碼至REMOTE端 |  |  |
| git branch branch name | 採用最新一次commit的版本 | git branch branch\_a |  |
| git log | 查看所有commit的歷史紀錄 |  |  |
| git checkout adb3238 | 切到某一個commit版本\(開一條branch\), \(checkout後面輸入commit代碼至少6碼\) | git checkout adb3238 | 切換\(CHECKOUT\) |
| git branch branch\_a | 在某一個commit版本\(adb3238\)開一條branch | git branch branch\_a |  |
| git branch -a | 查看目前我們開的所有branch | git branch -a |  |
| git branch -d | 刪除branch | git branch-dbranch\_a |  |
| git checkout master | 回到想要merge過去的主幹道上 |  | 切換\(CHECKOUT\) |
| git merge branch\_a | 把branch再融合回去主要的開發幹道上 | git merge branch\_a |  |
| git--help |  | git--help |  |
| git help |  | git help |  |
| git checkout–help |  | git checkout–help |  |
| git help checkout |  | git help checkout |  |
| git help checkout |  | git checkout\[-q\]\[-f\]\[-m\]\[\] |  |
| git help checkout |  | git checkout\[-q\]\[-f\]\[-m\]--detach\[\] |  |
| git help checkout |  | git checkout\[-q\]\[-f\]\[-m\]\[--detach\] |  |
| git help checkout |  | git checkout\[-q\]\[-f\]\[-m\]\[\[-b\|-B\|--orphan\]\]\[\] |  |
| git help checkout |  | git checkout\[-f\|--ours\|--theirs\|-m\|--conflict= |  |

---

#### Reference:

* [Git新手入門教學 – part 1 – 寫點科普，請給指教。](https://hellolynn.hpd.io/2017/01/18/git新手入門教學-part-1/)
* [Git新手入門教學 – part 2 – 寫點科普，請給指教。](https://hellolynn.hpd.io/2017/01/18/git新手入門教學-part-2/)

* [Git 與 Github 版本控制基本指令與操作入門教學 \| TechBridge 技術共筆部落格](https://blog.techbridge.cc/2018/01/17/learning-programming-and-coding-with-python-git-and-github-tutorial/)

* [What is version control \| Atlassian Git Tutorial](https://www.atlassian.com/git/tutorials/what-is-version-control)

* [What is Git: become a pro at Git with this guide \| Atlassian Git Tutorial](https://www.atlassian.com/git/tutorials/what-is-git#performance)

* [Why Git \| Atlassian Git Tutorial](https://www.atlassian.com/git/tutorials/why-git)



