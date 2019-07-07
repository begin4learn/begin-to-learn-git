### Git 內部運作原理

* #### Git 內部原理

  * 用檔案內容來定位的檔案系統
  * SHA1 是根據內容產生的，跟檔名無關
  * 內容一樣的檔案，即使檔案名稱不同，在Repository裡仍然只存一份。
  * 解耦合\(decouple\): 內容與當時的檔名


* Git 的 Repository 又稱作 Object Database 資料庫，共有四種 Objects 類型：

  * Blob 記錄檔案內容
  * Tree 記錄該目錄下有哪些檔案\(檔名、內容的SHA1\)和 Trees
  * Commit 記錄 commit 訊息、Root tree 和 Parent commits 的 SHA1
  * Tag 記錄標籤
  

* SHA-1 \(Secure Hash Algorithm 1 安全雜湊演算法1\)

  * 一種單向 Hash 雜湊加密演算法，例如它會將hello字串單向加密成為aaf4c61ddcc5e8a2dabede0f3b482cd9aea9434d。
  * 一種密碼雜湊函式，美國國家安全局設計，並由美國國家標準技術研究所（NIST）發布為聯邦資料處理標準（FIPS）
  * SHA-1可以生成一個被稱為訊息摘要的160位（20位元組）雜湊值，雜湊值通常的呈現形式為40個十六進位數。
  * 這個演算法有以下特性：
    * 給定 message 容易計算出 hash
    * 極度困難從 hash 推回 message
    * 極度困難修改 message 而 hash 不變
    * 極度困難不同的 messages 而 hash 一樣
    * hash 的分布很分散，跟 message 關聯不大

* #### Git 內部如何儲存檔案
    
![](/assets/觀察 Git 內部如何儲存檔案.jpg)

* #### Git 內部如何儲存 Commit

![](/assets/觀察 Git 內部如何儲存 Commit.jpg)

* #### 參照 Reference

  - Reference 會指向一個 Commit
  - tag 不會移動，指向的 commit 都一樣
    - 帶有額外資訊的 tag 內部會用 Object 儲存
  - branch 指向該 branch 最新的 commit
  - HEAD 指向 current branch

- Reference 是非常便宜的。
- 開新 branch 和 tag 只不過是 refs 而已，直到真的有 commit 前都沒有什麼負擔。
- 不像有些 CSV 開分支會複製一份原始碼，非常耗費資源。

* #### Integrity

  - SHA1 是內容的 checksum
  - Integrity: 如果檔案內容有損毀，就會發現跟SHA1不同。如果 tree 改檔名，也會被發現。
  - 這在分散式系統非常重要：資料從一個開發者傳到另一個開發者時，確保資料沒有被修改

* #### Git 內部如何儲存 Branch 分支



>cat .git/HEAD 拿到目前工作目錄 current branch 是指向哪一個 branch  
>cat .git/refs/heads/master 拿到 master branch 指向的 commit  
>cat .git/refs/tags/foobar 拿到 foobar tag 指向的 commit  



了解了 Git 如何儲存 Branch 之後，就再也不會想用中央儲存式的 SVN 了：  
- svn 開分支和 merge 超痛苦，能避免開 branch 就避免開 branch  
- svn 看 log 超痛苦，需要等待網路連線  
- svn commit 或 checkout 超慢，主機如果放國外常 commit 一半中斷



---

#### Reference:

* [Git 內部原理\( Git 版本控制系統 Git 簡介 by ihower 的 Git 教室\)](https://ihower.tw/git/internal.html)



