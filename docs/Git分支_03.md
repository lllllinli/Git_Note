#Git分支#
<br>
## 1.查看分支 ##

`````
$git branch

`````
##2.新增分支##

`````
$git branch <branchName>

`````
##3.切換分支##

`````
//修改測試

$git checkout <branchName>

`````
##4.合併分支##

`````
$git rebase <branchName>
$git merge <branchName>

`````

##5.處理合併衝突##

`````
$git merge <branchName>

// 出現confict 時的處理步驟：

// 將發生 confict 的檔案打開，處理內容( 別忘了刪除<<<、===、>>> )。
// 使用 git add 將處理好的檔案加入 stage。
// 反覆步驟 1~2 直到所有 confict 處理完畢。
// git commit 提交合併訊息。
// 完成

`````

####參考資料####
1.git-scm。[http://git-scm.com/book/zh-tw/%E9%96%8B%E5%A7%8B-%E5%88%9D%E6%AC%A1%E8%A8%AD%E5%AE%9AGit](http://git-scm.com/book/zh-tw/%E9%96%8B%E5%A7%8B-%E5%88%9D%E6%AC%A1%E8%A8%AD%E5%AE%9AGit)
2.ihower - Git 版本控制系統。[ihower - Git 版本控制系統](http://ihower.tw/git/intro.html)


