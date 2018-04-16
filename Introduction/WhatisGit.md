### What is git

Git 的物件結構，藏在一個名為 .git 的目錄裡面

- Blob
- Tree
- Commit
- Tag

- Git 特別的設計，在於它並
    - 不是記錄版本的差異，
    - 記錄檔案內容的「快照」（snapshot）
        - 讓 Git 在非常快速的切換版本


- *基本名詞*
    - Repository (數據庫/版本儲存庫)
        - 用來保存歷史程式碼，和所有跑這個專案需要的東西，包括所有原始碼、範例設計檔、文件等等。
 
    - Local (本地端)
        - 通常是個人開發的電腦/機台。
 
    - Remote (遠端)
        - 通常是一個共用的伺服器。

                                                                                                                                
- Git 的缺點
    - 易學難精
        - Git 的指令有非常多，而且有的指令有點複雜
        - 平常會用到的指令不太多，根據「80/20 法則」，大概 20% 的指令就足以應付 80% 的工作。
        
- Git 只關心檔案的「內容」，所以只要是檔案，其實都可以使用 Git 來管理。
- 設計師工作產出的檔案大多是 PhotoShop 的 PSD 或是 Illustractor 的 AI 檔，雖然 Git 也可以管理這些檔案，但因為這些檔案（二進位檔）不像一般文字檔可以一行一行的被檢視，所以就沒辦法那麼精準的知道什麼人在什麼時候改了哪些字。
- 使用 Git 還是可以幫得上設計師的忙，至少當檔案不小心被覆蓋或刪除的時候，還可以救回舊的版本的檔案。


- Git
    - 版本控制軟體

        
- GitHub
    - 一個商業網站，本體是一個 Git 伺服器
    - 這個網站上的應用程式讓大家可以透過 Web 介面來操作一些原本需要複雜的 Git 指令才能做到的事。


----
#### Reference:
- [什麼是 Git？為什麼要學習它？ 為你自己學 Git](https://gitbook.tw/chapters/introduction/what-is-git.html)
    - [與其它版本控制系統的差異 為你自己學 Git](https://gitbook.tw/chapters/introduction/difference-between-other-system.html)
- [What is Git: become a pro at Git with this guide | Atlassian Git Tutorial](https://www.atlassian.com/git/tutorials/what-is-git#performance)
