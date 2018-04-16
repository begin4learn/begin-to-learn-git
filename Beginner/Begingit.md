### Begin git step by step

##### 

##### 01. 安裝並且設定Git

* 任務1：安裝Git到你的電腦上，並且設定好Git內部的使用者名稱和電子信箱

| 安裝Git | Windows | Mac | Linux |
| :--- | :--- | :--- | :--- |
| 方法1 | 下載安裝cmder模擬Linux terminal終端機,選擇完整版本就會順便安裝 |  | Debian: apt-get install git Fedora: yum install git-core |
| 方法2 | 到Git官網安裝\([https://git-scm.com/downloads\](https://git-scm.com/downloads%29\) | 到Git官網安裝\([https://git-scm.com/downloads\](https://git-scm.com/downloads%29\) | 到Git官網安裝\([https://git-scm.com/downloads\](https://git-scm.com/downloads%29\) |
| 方法3 | Github當作遠端托管程式的環境 | 根據作業系統安裝Github桌面版當作操作工具（內建安裝Git） |  |
| Check是否安裝成功 | git --version | git --version | git --version |
| 設定Git內部的使用者名稱 | git config --global user.name "&lt;Your Name&gt;" | git config --global user.name "&lt;Your Name&gt;" | git config --global user.name "&lt;Your Name&gt;" |
| 設定Git內部的電子信箱 | git config --global user.email "&lt;your@gmail.com&gt;" | git config --global user.email "&lt;your@gmail.com&gt;" | git config --global user.email "&lt;your@gmail.com&gt;" |
|  |  |  |  |

##### 

##### 02. 建立一個本機的 repository \(local repositories\)

* 任務二：在自己的電腦上建立一個新的 local repositories（本地檔案庫）
  * repository（檔案庫）: 就是一個專案，又簡稱repo。
    * 以電腦的檔案資料管理來看，我們通常會把同一個專案的資料放到同一個資料夾下，
    * 可以把repository看成一個資料夾。

| command |  |  |
| :--- | :--- | :--- |
| mkdir hello-git | 建立一個hello-git資料夾 |  |
| cd hello-git | 移動到hello-git資料夾 |  |
| git init | 將專案資料夾建立成git repository |  |
| ls -la | 列出專案資料夾下的檔案和資料夾 | -l參數為列出詳細資料 -a為列出隱藏資料夾 |

##### 

##### 03. 檢視狀態、新增或修改 commits

* 任務三：在你的repository檔案庫中建立一個新檔案，新增一些內容到該檔案並且將那些檔案修改提交commit到Git中
  * 使用文字編輯器，新增一個hello.py的檔案
    * 一個會印出hello python & git字串的python程式

| command |  | result |  |
| :--- | :--- | :--- | :--- |
| Edit hello.py1 |  | print\('hello python & git'\) |  |
| git status | 我們有新增新的檔案，但是還沒進到git追蹤範圍中/暫存區，使用git add hello.py加入追蹤，這樣之後檔案有修改就可以追蹤到。 | On branch masterInitial commitUntracked files:\(use "git add &lt;file&gt;..." to include in what will be committed\)hello.pynothing added to commit but untracked files present \(use "git add" to track\) |  |
| git add hello.py | 加入stage追蹤hello.py |  |  |
| git status | On branch masterInitial commitChanges to be committed:\(use "git rm --cached &lt;file&gt;..." to unstage\)new file: hello.py |  |  |
| git diff | 比較現在檔案和上次commit之間的差異，也就是說你做了哪些修改 |  |  |
| git commit -m "Init hello.py" | -m為輸入commit message，也就是說這個commit內做了哪些事情 | \[master \(root-commit\) ad6d328\] Init hello.py1 file changed, 1 insertion\(+\)create mode 100644 hello.py |  |
| git status |  | On branch masternothing to commit, working tree clean |  |
| git rm --cached hello.py | 檔案尚未加入過追蹤時使用，即可恢復到檔案尚未加入暫存區 |  | 反悔不想把檔案加入追蹤 |
| git reset HARD | 檔案已經在repository內 | repository與stage的檔案都會被還原到HEAD，但working directory內的檔案不變 | 反悔不想把檔案加入追蹤 |
| Edit hello.py |  | print\('hello python & git rock'\) |  |
| git add hello.py | 加入stage追蹤hello.py |  |  |
| git checkout -- hello.py | 放棄修改 |  |  |
| git diff | 比較現在檔案和上次commit之間的差異，也就是說你做了哪些修改 |  |  |
| git status | 查看目前工作狀態 | Changes not staged for commit:\(use "git add &lt;file&gt;..." to update what will be committed\)\(use "git checkout -- &lt;file&gt;..." to discard changes in working directory\) modified: hello.py |  |
| git commit -a -m "修改了hello.py" | 簡寫commit這個修改 |  | -a是add，-m為message簡寫，後面接訊息資訊 |
|  |  |  |  |

##### 

##### 04. 註冊 GitHub 帳號

* 任務四：建立一個GitHub帳號，並在Git設定中加入使用者帳號\`
  * 透過github當作我們remote工作環境,管理程式碼
    * 和其他開發者一起合作，參與開放原始碼的開發。  
    * github若是公開的repo是無限制數量免費的
    * 使用private repo可以參考付費方案。

| Process |  |  |
| :--- | :--- | :--- |
| github.com註冊帳號 |  |  |
| 點選右上角+來新增new repository（檔案庫） |  |  |
| 輸入repository name（你要取的專案名稱） | git-example | 跟電腦local專案一致 |
| 輸入簡短專案描述 |  |  |
| 不勾選初始化README |  | 會造成本地端和遠端不一致會需要額外一些處理 |
| 不要選擇.gitignore | 要忽略的檔案清單:告訴Git，當在做版本控制記錄的時候，忽略這些檔案 | 會造成本地端和遠端不一致會需要額外一些處理 |
| .gitignore | 通常一些機密資料，如資料庫帳號密碼或是server IP位置等，記得要加入 | 參考github上面的一些範本在新增repository時選取對應的程式語言 |
| 不要選擇License授權 | 專案使用何種授權方式 | 例如：MIT、BSD等 |
| README.md | README.md：repository介紹和使用方式說明（例如：使用方法、參與專案方式等） | 使用markdown語法撰寫 |
| CONTRIBUTING.md | 說明如何參與貢獻 |  |
| 按create按鈕 | 新增成功，創建了自己第一個github repository（遠端檔案庫）！ |  |
|  |  |  |

##### 

##### 05. 將 repository 做本機和遠端的連結

* 任務五：把電腦裡Local（本地端）的repository（檔案庫）和remote（遠端）的repository（檔案庫）連結起來，並push電腦上的修改

| Command |  | result |  |
| :--- | :--- | :--- | :--- |
| git remote add origin &lt;remote網址&gt; | 本地端專案加入origin對應到遠端網址 | 加入remote網址 |  |
| $ git status | 觀看情況 |  |  |
| git push -u origin master | 將本地端程式push到遠端檔案庫 | Counting objects: 3, done.Writing objects: 100% \(3/3\), 239 bytes \| 0 bytes/s, done.Total 3 \(delta 0\), reused 0 \(delta 0\)To [https://github.com/happycodergit/git-example.git\*](https://github.com/happycodergit/git-example.git*) \[new branch\] master -&gt; masterBranch master set up to track remote branch master from origin. | git push -u &lt;remote name&gt;&lt;branch name&gt;-u等同於--set-upstream只要做過一次，並成功push出去；本機端的master就會被設定去追蹤遠端的&lt;remote name&gt;/&lt;branch name&gt;分支。只要成功設定好upstream後，第二次以後要上傳分支時，就只需要透過git push就可以了，不必再帶&lt;remote name&gt;跟&lt;branch name&gt;等參數 |
| git push |  |  | 第二次以後要上傳分支，不必再帶&lt;remote name&gt;跟&lt;branch name&gt;等參數 |
| git push -u origin master | 可以拆解成 |  | git push origin master         git checkout master           git branch -u origin/master |
|  |  |  |  |

##### 

##### 06. Fork 和 clone 一個 open source（開源）的計畫

* 任務六：從 GitHub.com 建立專案，複本 fork，並下載 clone到電腦上

| Process |  |
| :--- | :--- |
| 點選左上角github icon回到首頁 |  |
| 搜尋欄搜尋react |  |
| 點選右上角fork按鈕，複製一份專案 |  |
| 點選右邊綠色按鈕clone download複製HTTP網址 |  |
| git clone [https://github.com/happycodergit/react.git](https://github.com/happycodergit/react.git) | 複製到本地端 |
| cd react | 移動到react資料夾 |
| git checkout -b happycoder@feature\_branch | 切出自己的新分支（使用-b） |
| Edit README.md | 做一些README.md檔案修改 |
| git commit -a -m "Update README" | ，然後commit到自己fork過來的專案 |
| git push origin happycoder@feature\_branch |  |
| 到原始專案頁面點選new pull request按鈕發pull request | （會比對程式碼的差異）。若對方review完後接受就可以將自己的程式碼合併到原始專案中，為開放原始碼做出第一步貢獻！ |
| git pull upstream master | 完成pull request記得讓master（或是合併進去的branch）保持同步 |
|  |  |

##### 

##### 07. 練習建立一個 feature branch

* `任務七：回來原來的 git-example 專案新增 feature branch (分支)`

| Command |  |  |
| :--- | :--- | :--- |
| git checkout -b dev | 建立一個名為dev的branch |  |
| Edit hello.oy | 在hello.py最上面多加一行\# hi, this is comment註解後存檔 |  |
| git commit -a -m "Init dev branch" | commit到本地端repository更新 |  |
| gut push origin dev |  |  |
|  |  |  |

##### 

##### 08. 邀請別人和你合作

* 任務八：在專案新增夥伴collaborator

| Command |  |  |
| :--- | :--- | :--- |
| 在右上角進入setting |  |  |
| 選擇到collaborator新增合作者 |  |  |
|  |  |  |

##### 

##### 09. 利用 push 和 pull 來和 GitHub.com 同步

* 任務九：用pull來和其他collaborators（合作者）同步更新，確保程式是最新的版本



| Process |  |  |  |
| :--- | :--- | :--- | :--- |
| git colone git-example專案 | 請其他開發者git colone下來你的git-example專案 |  |  |
|  | checkout到dev branch |  |  |
|  | 完成新增一個README.md檔案 |  |  |
|  | 發pull request過來 |  |  |
|  | 沒問題就按同意並合併 |  |  |
| git pull origin dev | 我們透過git pull來保持本地端和遠端程式碼同步 |  |  |
|  |  |  |  |



##### 10. Merge（合併）和刪除 branches

* 任務十：在本機上merge合併你的branch（分支），刪除舊的branch（分支）



| process |  |  |
| :--- | :--- | :--- |
| git checout master | 移動到master branch |  |
| git merge dev | 合併dev到master |  |
| git branch -d dev | 刪除dev branch |  |
| git push origin master | 將合併後的master推送到遠端 |  |
|  |  |  |



---

#### Reference:

* ##### installation & setup

  * [Git 與 Github 版本控制基本指令與操作入門教學 \| TechBridge 技術共筆部落格](https://blog.techbridge.cc/2018/01/17/learning-programming-and-coding-with-python-git-and-github-tutorial/)

  * [Git新手入門教學 – part 1 – 寫點科普，請給指教。](https://hellolynn.hpd.io/2017/01/18/git新手入門教學-part-1/)

  * [Git新手入門教學 – part 2 – 寫點科普，請給指教。](https://hellolynn.hpd.io/2017/01/18/git新手入門教學-part-2/)

