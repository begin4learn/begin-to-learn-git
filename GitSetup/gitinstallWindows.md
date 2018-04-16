### git install/ Windows

- #### install git

* [到官方網站下載合適的版本](http://git-scm.com/downloads)

```
https://git-scm.com/download/win
```

* 安裝完成，打開「Git Bash」應用程式

  * 驗證 Git 是不是有安裝起來

```
which git

git --version

```

- 看到類似的訊息，安裝成功
  - which git = > /mingw64/bin/git
  - git --version => git version 2.14.1.windows.1


- #### [install GUI Clients 圖形化介面工具](https://git-scm.com/downloads/guis)

  - SourceTree 
  - GitHub Desktop
  - Mac 以及 Windows 作業系統都有，免費


- #### git setup


```
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
git config --global color.ui true

git config --global core.editor vi
或 git config --global core.editor gedit

```

- Windows 平台對於換行字元的處理與 Unix/Mac 平台不同，會讓 Git 誤判成有修改，因此需要多以下設定：


```
git config --global core.autocrlf true
git config --global core.safecrlf true
```

- #### 產生 SSH key：

```
ssh-keygen -t rsa -C "your_email@example.org"
```

- #### Public SSH key。

```
用文字編輯器打開 “%homedrive%%homepath%.ssh\id_rsa.pub” 的內容
```

- #### Github 開專案

    - Public SSH key 複製下來貼到 Github 帳號 -> Account Settings -> SSH Keys 裡
    - 可以 push 和 pull 下來


---

#### Reference:

* [安裝在 Windows 作業系統 \(from 為你自己學 Git\)](https://gitbook.tw/chapters/environment/install-git-in-windows.html)

* [Git - Git 安裝教學](https://git-scm.com/book/zh-tw/v2/開始-Git-安裝教學)

* [Git 簡介與安裝 \(by 張文鈿 a.k.a. ihower\)](https://ihower.tw/git/intro.html)

* [Install Git \| Atlassian Git Tutorial](https://www.atlassian.com/git/tutorials/install-git)




