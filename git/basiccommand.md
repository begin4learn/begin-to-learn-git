### Tools/Basic Linux Command 

##### [常用命令列指令 (from 為你自己學 Git by 五倍紅寶石 高見龍)](https://gitbook.tw/chapters/command-line/command-line.html)

- 終端機環境常會用到的系統指令。

| Windows | MacOS / Linux | 說明 |
| :--- | :--- | :--- |
| cd | cd | 切換目錄 |
| cd | pwd | 取得目前所在的位置 |
| dir | ls | 列出目前的檔案列表 |
| mkdir | mkdir | 建立新的目錄 |
| 無 | touch | 建立檔案 |
| copy | cp | 複製檔案 |
| move | mv | 移動檔案 |
| del | rm | 刪除檔案 |
| cls | clear | 清除畫面上的內容 |

不同的作業系統，指令也會不太一樣。

#### 目錄切換及顯示

- 指令要在正確的目錄下才能正常運作

```
# 切換到 /tmp 目錄（絕對路徑）
$ cd /tmp

# 切換到 my_project 目錄（相對路徑）
$ cd my_project

# 往上一層目錄移動
$ cd ..

# 切換到使用者的 home 目錄中的 project 裡的 namecards 目錄
# 這個 "~" 符號表示 home 目錄
$ cd ~/project/namecards/

# 顯示目前所在目錄
$ pwd
/tmp

```

- #####Windows：

```
# 切換到 D 槽的 5xruby 目錄（絕對路徑）
C:\
>
 cd D:\5xruby

# 切換到 5xruby 目錄（相對路徑）
D:\
>
 cd 5xruby

# 往上一層目錄移動
D:\5xruby
>
 cd ..

# 顯示目前所在目錄
D:\5xruby
>
 cd
D:\5xruby

```

#### 檔案列表

- `ls`指令可列出在目前目錄所有的檔案及目錄
 - `-al`參數
    - `a` 小數點開頭的檔案（例如.gitignore）也會顯示
    - `l` 完整檔案的權限、擁有者以及建立、修改時間

```
$ ls -al
total 56
drwxr-xr-x  18 user  wheel   612 Dec 18 02:20 .
drwxrwxrwt  24 root  wheel   816 Dec 18 02:19 ..
-rw-r--r--   1 user  wheel   543 Dec 18 02:19 .gitignore
-rw-r--r--   1 user  wheel  1729 Dec 18 02:19 Gemfile
-rw-r--r--   1 user  wheel  4331 Dec 18 02:20 Gemfile.lock
-rw-r--r--   1 user  wheel   374 Dec 18 02:19 README.md
-rw-r--r--   1 user  wheel   227 Dec 18 02:19 Rakefile
drwxr-xr-x  10 user  wheel   340 Dec 18 02:19 app
drwxr-xr-x   8 user  wheel   272 Dec 18 02:20 bin
drwxr-xr-x  14 user  wheel   476 Dec 18 02:19 config
-rw-r--r--   1 user  wheel   130 Dec 18 02:19 config.ru
drwxr-xr-x   4 user  wheel   136 Dec 18 02:41 db
drwxr-xr-x   4 user  wheel   136 Dec 18 02:19 lib
drwxr-xr-x   4 user  wheel   136 Dec 18 02:23 log
drwxr-xr-x   9 user  wheel   306 Dec 18 02:19 public
drwxr-xr-x   9 user  wheel   306 Dec 18 02:19 test
drwxr-xr-x   7 user  wheel   238 Dec 18 02:23 tmp
drwxr-xr-x   3 user  wheel   102 Dec 18 02:19 vendor

```

#### 建立檔案、目錄

```
$ touch index.html

```

- 如果 index.html 這個檔案本來不存在，`touch`指令會建立一個名為 index.html 的空白檔案；
- 如果本來就已經存在，則只會改變這個檔案的最後修改時間，不會變更原本這個檔案的內容。

```
$ mkdir demo

```

`mkdir`指令會在目前所在目錄，建立一個名為 demo 的目錄。

#### 檔案操作 

把檔案 index.html 複製一份成 about.html：

```
$ cp index.html about.html

```

把檔案 index.html 更名成 info.html：

```
$ mv index.html info.html

```

刪除檔案 index.html：

```
$ rm index.html

```

刪除在這個目錄裡所有的 html 檔：

```
$ rm *.html

```

在 Windows 作業系統則是把`cp`、`mv`以及`rm`指令分別換成`copy`、`move`以及`del`。

----

#### Reference

* [終端機及常用指令介紹 (from 為你自己學 Git by 五倍紅寶石 高見龍)](https://gitbook.tw/chapters/command-line/command-line.html)
* [終端機及常用指令介紹 - 為你自己學 Git | 高見龍](https://gitbook.tw/chapters/command-line/command-line.html)








