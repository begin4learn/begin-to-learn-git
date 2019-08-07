### git setup

#### Setup

![Git Tutorial - by 張文鈿 a.k.a. ihower](/assets/Screen Shot 2017-03-11 at 22.19.59.png)
- from: Git Tutorial - by 張文鈿 a.k.a. ihower

- #### git setup


```
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
git config --global color.ui true

git config --global core.editor vi
或 git config --global core.editor gedit

```


- #### git alias

    - 編輯 ~/.gitconfig



```
[alias]
    co = checkout
    ci = commit
    st = status
    br = branch -v
    rt = reset --hard
    unstage = reset HEAD
    uncommit = reset --soft HEAD^
    l = log --pretty=oneline --abbrev-commit --graph --decorate
    amend = commit --amend
    who = shortlog -n -s --no-merges
    g = grep -n --color -E
    cp = cherry-pick -x
    nb = checkout -b

    # 'git add -u' handles deleted files, but not new files
    # 'git add .' handles any current and new files, but not deleted
    # 'git addall' now handles all changes
    addall = !sh -c 'git add . && git add -u'

    # Handy shortcuts for rebasing
    rc = rebase --continue
    rs = rebase --skip
    ra = rebase --abort

```


- #### 命令列(Bash)提示
    - 編輯 ~/.bashrc
    


```
function git_branch {
  ref=$(git symbolic-ref HEAD 2> /dev/null) || return;
  echo "("${ref#refs/heads/}") ";
}

function git_since_last_commit {
  now=`date +%s`;
  last_commit=$(git log --pretty=format:%at -1 2> /dev/null) || return;
  seconds_since_last_commit=$((now-last_commit));
  minutes_since_last_commit=$((seconds_since_last_commit/60));
  hours_since_last_commit=$((minutes_since_last_commit/60));
  minutes_since_last_commit=$((minutes_since_last_commit%60));

  echo "${hours_since_last_commit}h${minutes_since_last_commit}m ";
}

PS1="[\[\033[1;32m\]\w\[\033[0m\]] \[\033[0m\]\[\033[1;36m\]\$(git_branch)\[\033[0;33m\]\$(git_since_last_commit)\[\033[0m\]$ "

```


----
- [Git 簡介與安裝 ( Git 版本控制系統  Git 簡介 by ihower 的 Git 教室)](https://ihower.tw/git/intro.html)

- [使用者設定 - 為你自己學 Git | 高見龍](https://gitbook.tw/chapters/config/user-config.html)
    - [其它方便的設定 - 為你自己學 Git | 高見龍](https://gitbook.tw/chapters/config/convenient-settings.html)
    
* [配置 · Git](https://zlargon.gitbooks.io/git-tutorial/content/config.html)
    
    
    