### Tools/git command

| git Command | Explain | syntax |  | Note |
| :--- | :--- | :--- | :--- | :--- |
| git--version | 確認是否安裝成功 |  |  |  |
| git config--globaluser.name"user name" | 告訴Git使用者資訊 | git config--globaluser.name"Lynn19931205" |  |  |
| git config--globaluser.email"email address" | 告訴Git使用者資訊 | git config--globaluser.email"j890355b@gmail.com" |  |  |
| git config–list | 看你的Git設定內容 |  |  |  |
| cd~/desktop$ | 至桌面 | cd~/desktop$mkdir project\_1 |  |  |
| mkdir project\_1 | 創建一個叫做project\_2的資料夾 |  |  |  |
| cd~/desktop/project\_1/ |  | cd~/desktop/project\_1/ |  |  |
| touch hello.txt | 創建一個名稱為hello.txt的文件 | touch hello.txt |  |  |
| git clone | clone下來別人的專案到local端 | gitclone[https://github.com/sarcadass/granim⋯⋯New\_Project](https://github.com/sarcadass/granim⋯⋯New_Project) |  |  |
| git init | 創建一個新的Repository\(打開任何一個專案資料夾打上git init\) |  |  |  |
| git status | 查看目前的Git狀態:「hello.txt」這個檔案還沒有被追蹤 |  |  | 查看目前狀 |
| git add主檔名.副檔名 | 將檔案提交入Staging Area | git add主檔名.副檔名 |  |  |
| git add | 將整個資料夾的檔案都一起推送上去到Staging Area | git add不輸入檔案名稱 |  | 進入暫存區\(ADD\) |
| git commit-m'一行解說文字' | 將Staging Area內的東西推到Repository成為正式的版本 | git commit-m'Add a line' |  | 提交版本\(COMMIT\) |
| git status | 工作區很乾淨噢，沒有新的修改、Staging Area裡面也沒有東西 |  |  | 查看目前狀 |
| git log | 查看所有的commit紀錄 |  |  | 查看目前狀 |
| git rm--cached | 將不在Repository的檔案移出Staging Area | git rm--cached hello.txt |  | 將檔案移出的暫存區 |
| git rm--cached | 檔案已經在repository內,從repository刪除，並且從stage刪除，檔案會從tracked變成untracked |  |  | 將檔案移出的暫存區 |
| git rm--cached | 檔案不在repository內,移除Staing Area中的檔案 |  |  | 將檔案移出的暫存區 |
| git reset HEAD檔案名稱 | 將已經在Repository的檔案,移出Staging Area |  |  | 將檔案移出的暫存區 |
| git diff | 比較文件或commit間修改的差異 |  |  | 查看目前狀 |
| git diff commit代碼 | 比較兩次commit間修改的差異 | git diff8a85090dc97a |  | 查看目前狀 |
| git log | 查看所有的commit紀錄: commit 8a85094b22edf4184e7228c3f849807dd7eed2c9 |  |  | 查看目前狀 |
| git show | 查看某項特定commit的修改內容,詳細列出該次commit的修改內容 | git show8a8509 |  | 第一欄的commit代碼複製起來\(複製六碼或以上\) |
| git status | 列出目前的檔案狀態 |  |  | 查看目前狀 |
| [打開 https://github.com/ 網站](https://l.facebook.com/l.php?u=https%3A%2F%2Fgithub.com%2F&h=ATP4pyBaH6lENbLvLZAk-sSNNu1wrO0HG9MxBGgjTpSL1_e0H9xpv3DVSVvKpXhvcRZ2R1BUc3lruNFY1OsXsc05BZu2DzJAoWL5-ZOTKchiqTpwX6qAsyeyv7glizoeMJGJtRKbqBy1&s=1) |  |  |  |  |
| 在GitHub上創建一個和本地端名稱相同的資料夾，專案描述可寫可不寫、權限設為開放、README不用勾選 |  |  |  |  |
| git remote add origin [https://github.com/Lynn19931205/project\_1.git](https://github.com/Lynn19931205/project_1.git) | 將Local端的程式碼推到GitHub網站 |  |  | repository已存在 |
| git push -u origin master | 將Local端的程式碼推到GitHub網站 |  |  | repository已存在 |
| git pull | 將程式碼從Remote端拉下來到Local端 |  |  |  |
| edit conflict |  |  |  |  |
| git add | 將整個資料夾的檔案都一起推送上去到Staging Area |  |  |  |
| git commit | 將Staging Area內的東西推到Repository成為正式的版本 |  |  |  |
| git push | push to GitHub,推送程式碼至REMOTE端 |  |  |  |
| git branch branch name | 採用最新一次commit的版本 | git branch branch\_a |  |  |
| git log | 查看所有commit的歷史紀錄 |  |  |  |
| git checkout adb3238 | 切到某一個commit版本\(開一條branch\), \(checkout後面輸入commit代碼至少6碼\) | git checkout adb3238 |  | 切換\(CHECKOUT\) |
| git branch branch\_a | 在某一個commit版本\(adb3238\)開一條branch | git branch branch\_a |  |  |
| git branch -a | 查看目前我們開的所有branch | git branch -a |  |  |
| git branch -d | 刪除branch | git branch-dbranch\_a |  |  |
| git checkout master | 回到想要merge過去的主幹道上 |  |  | 切換\(CHECKOUT\) |
| git merge branch\_a | 把branch再融合回去主要的開發幹道上 | git merge branch\_a |  |  |
| git --help |  | git--help |  |  |
| git help |  | git help |  |  |
| git checkout–help |  | git checkout–help |  |  |
| git help checkout |  | git help checkout |  |  |
| git help checkout |  | git checkout\[-q\]\[-f\]\[-m\]\[\] |  |  |
| git help checkout |  | git checkout\[-q\]\[-f\]\[-m\]--detach\[\] |  |  |
| git help checkout |  | git checkout\[-q\]\[-f\]\[-m\]\[--detach\] |  |  |
| git help checkout |  | git checkout\[-q\]\[-f\]\[-m\]\[\[-b\|-B\|--orphan\]\]\[\] |  |  |
| git help checkout |  | git checkout\[-f\|--ours\|--theirs\|-m\|--conflict= |  |  |

---

### Git Beginner A-Z

| git command | Explain | syntax |  | Note |
| :--- | :--- | :--- | :--- | :--- |
| cd~/desktop$ | 至桌面 | cd~/desktop$mkdirproject\_1 |  |  |
| cd~/desktop/project\_1/ |  | cd~/desktop/project\_1/ |  |  |
| edit conflict |  |  |  |  |
| git clone | clone下來別人的專案到local端 | gitclone[https://github.com/sarcadass/granim⋯⋯New\_Project](https://github.com/sarcadass/granim⋯⋯New_Project) |  |  |
| git add | 將整個資料夾的檔案都一起推送上去到Staging Area | gitadd不輸入檔案名稱 |  | 進入暫存區\(ADD\) |
| git add | 將整個資料夾的檔案都一起推送上去到Staging Area |  |  |  |
| git add主檔名.副檔名 | 將檔案提交入Staging Area | gitadd主檔名.副檔名 |  |  |
| git branch -a | 查看目前我們開的所有branch | gitbranch -a |  |  |
| git branch branchname | 採用最新一次commit的版本 | gitbranchbranch\_a |  |  |
| git branch branch\_a | 在某一個commit版本\(adb3238\)開一條branch | gitbranchbranch\_a |  |  |
| git branch -d | 刪除branch | gitbranch-dbranch\_a |  |  |
| git checkout adb3238 | 切到某一個commit版本\(開一條branch\), \(checkout後面輸入commit代碼至少6碼\) | gitcheckout adb3238 |  | 切換\(CHECKOUT\) |
| git checkout –help |  | gitcheckout–help |  |  |
| git checkout master | 回到想要merge過去的主幹道上 |  |  | 切換\(CHECKOUT\) |
| git commit | 將Staging Area內的東西推到Repository成為正式的版本 |  |  |  |
| git commit -m '一行解說文字' | 將Staging Area內的東西推到Repository成為正式的版本 | gitcommit-m'Add a line' |  | 提交版本\(COMMIT\) |
| git config --global user.email "email address" | 告訴Git使用者資訊 | gitconfig--globaluser.email"j890355b@gmail.com" |  |  |
| git config -global user.name "user name" | 告訴Git使用者資訊 | gitconfig--globaluser.name"Lynn19931205" |  |  |
| git config –list | 看你的Git設定內容 |  |  |  |
| git diff | 比較文件或commit間修改的差異 |  |  | 查看目前狀 |
| git diff commit代碼 | 比較兩次commit間修改的差異 | gitdiff8a85090dc97a |  | 查看目前狀 |
| git help |  | githelp |  |  |
| git help checkout |  | githelp checkout |  |  |
| git help checkout |  | gitcheckout\[-q\]\[-f\]\[-m\]\[\] |  |  |
| git help checkout |  | gitcheckout\[-q\]\[-f\]\[-m\]--detach\[\] |  |  |
| git help checkout |  | gitcheckout\[-q\]\[-f\]\[-m\]\[--detach\] |  |  |
| git help checkout |  | gitcheckout\[-q\]\[-f\]\[-m\]\[\[-b\|-B\|--orphan\]\]\[\] |  |  |
| git help checkout |  | gitcheckout\[-f\|--ours\|--theirs\|-m\|--conflict= |  |  |
| git init | 創建一個新的Repository\(打開任何一個專案資料夾打上gitinit\) |  |  |  |
| git log | 查看所有的commit紀錄 |  |  | 查看目前狀 |
| git log | 查看所有的commit紀錄: commit 8a85094b22edf4184e7228c3f849807dd7eed2c9 |  |  | 查看目前狀 |
| git log | 查看所有commit的歷史紀錄 |  |  |  |
| git merge branch\_a | 把branch再融合回去主要的開發幹道上 | gitmergebranch\_a |  |  |
| git pull | 將程式碼從Remote端拉下來到Local端 |  |  |  |
| git push | push to GitHub,推送程式碼至REMOTE端 |  |  |  |
| git push -u origin master | 將Local端的程式碼推到GitHub網站 |  |  | repository已存在 |
| git remote add origin [https://github.com/Lynn19931205/project\_1.git](https://github.com/Lynn19931205/project_1.git) | 將Local端的程式碼推到GitHub網站 |  |  | repository已存在 |
| git reset HEAD 檔案名稱 | 將已經在Repository的檔案,移出Staging Area |  |  | 將檔案移出的暫存區 |
| git rm--cached | 將不在Repository的檔案移出Staging Area | gitrm--cached hello.txt |  | 將檔案移出的暫存區 |
| git rm--cached | 檔案已經在repository內,從repository刪除，並且從stage刪除，檔案會從tracked變成untracked |  |  | 將檔案移出的暫存區 |
| git rm--cached | 檔案不在repository內,移除StaingArea中的檔案 |  |  | 將檔案移出的暫存區 |
| git show | 查看某項特定commit的修改內容,詳細列出該次commit的修改內容 | gitshow8a8509 |  | 第一欄的commit代碼複製起來\(複製六碼或以上\) |
| git status | 查看目前的Git狀態:「hello.txt」這個檔案還沒有被追蹤 |  |  | 查看目前狀 |
| git tatus | 工作區很乾淨噢，沒有新的修改、Staging Area裡面也沒有東西 |  |  | 查看目前狀 |
| git status | 列出目前的檔案狀態 |  |  | 查看目前狀 |
| git --version | 確認是否安裝成功 | git --version |  | git version 2.14.1 |
| git --help |  | git--help |  |  |
| mkdir project\_1 | 創建一個叫做project\_2的資料夾 |  |  |  |
| touch hello.txt | 創建一個名稱為hello.txt的文件 | touch hello.txt |  |  |
| [打開 https://github.com/ 網站](https://l.facebook.com/l.php?u=https%3A%2F%2Fgithub.com%2F&h=ATP4pyBaH6lENbLvLZAk-sSNNu1wrO0HG9MxBGgjTpSL1_e0H9xpv3DVSVvKpXhvcRZ2R1BUc3lruNFY1OsXsc05BZu2DzJAoWL5-ZOTKchiqTpwX6qAsyeyv7glizoeMJGJtRKbqBy1&s=1) |  |  |  |  |
| 在GitHub上創建一個和本地端名稱相同的資料夾，專案描述可寫可不寫、權限設為開放、README不用勾選 |  |  |  |  |

---

#### Reference:

* [Git新手入門教學 – part 1 – 寫點科普，請給指教。](https://hellolynn.hpd.io/2017/01/18/git新手入門教學-part-1/)
* [Git新手入門教學 – part 2 – 寫點科普，請給指教。](https://hellolynn.hpd.io/2017/01/18/git新手入門教學-part-2/)

* [What is version control \| Atlassian Git Tutorial](https://www.atlassian.com/git/tutorials/what-is-version-control)

* [What is Git: become a pro at Git with this guide \| Atlassian Git Tutorial](https://www.atlassian.com/git/tutorials/what-is-git#performance)

* [Why Git \| Atlassian Git Tutorial](https://www.atlassian.com/git/tutorials/why-git)

* [終端機及常用指令介紹 - 為你自己學 Git \| 高見龍](https://gitbook.tw/chapters/command-line/command-line.html)



