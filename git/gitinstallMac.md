### git install/Mac


- #### install git

##### Method 1: [從官方網站下載 Mac 專屬版本的 Git](http://git-scm.com/downloads)

```
https://git-scm.com/download/mac
```


##### Method 2: 使用 Homebrew 軟體來安裝 Git

    - [homebrew: macOS 缺少的套件管理工具](https://brew.sh/index_zh-tw)

- [安裝 homebrew](https://brew.sh/index_zh-tw.html): 終端機視窗貼上並執行

```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

- [Installation — Homebrew Documentation](https://docs.brew.sh/Installation)

```
mkdir homebrew && curl -L https://github.com/Homebrew/brew/tarball/master | tar xz --strip 1 -C homebrew
```

- install git


```
brew install git
```

- #### [install GUI Clients 圖形化介面工具](https://git-scm.com/downloads/guis)

    - SourceTree 
    - GitHub Desktop
    - Mac 以及 Windows 作業系統都有，免費


- #### 產生 SSH key：

```
ssh-keygen -t rsa -C "your_email@youremail.com"
```

- #### Public SSH key。

```
cat ~/.ssh/id_rsa.pub
```

- #### Github 開專案

    - Public SSH key 複製下來貼到 Github 帳號 -> Account Settings -> SSH Keys 裡
    - 可以 push 和 pull 下來












----
#### Reference: 

- [安裝在 Mac OSX 作業系統 (from 為你自己學 Git)](https://gitbook.tw/chapters/environment/install-git-in-mac.html)

- [Git - Git 安裝教學](https://git-scm.com/book/zh-tw/v2/開始-Git-安裝教學)
- [Git 簡介與安裝 (by 張文鈿 a.k.a. ihower)](https://ihower.tw/git/intro.html)

- [Install Git | Atlassian Git Tutorial](https://www.atlassian.com/git/tutorials/install-git)


