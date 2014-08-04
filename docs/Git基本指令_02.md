#Git基本指令#
<br>
## 1. 在本機建立一個 repository ##

`````
/*
* 首次建立 Git 專案
*
* 1.移動路徑到'專案資料夾'。
* 2.建立一個Git_Test專案目錄。
* 3.移動到'專案資料夾'下。
* 4.產生一個新的 repository。
*/

$cd 資夾路徑 
$mkdir 專案名稱
$cd 專案名稱
$git init


`````
##2.第一次 Commit##

`````
/*
* 第一次 Commit
*
* 1.建立一個 README.md 檔。
* 2.把 README 加入到工作區。
* 3.檢察工作區狀態。
* 4.Commit 。
*/

$touch README
$git add README
$git status
$git commit -m “First Commit”

`````

##3.修改檔案##

`````
/*
* 修改檔案流程
*
* 1.檢察工作區狀態。
* 2.檢查衝突
* 3.檢察工作區狀態。
* 4.Commit 加註解。
*/

編輯 README 做些變更
$git status
$git diff
$git add .  	(一次加入所有變更跟新增檔案，但不包括刪除的檔案!)
$git status
$git diff --cached
$git commit -m “Update README”

`````

##3.回復前一個版本##

`````
$git reset HAND

`````





####參考資料####
1.git-scm。[http://git-scm.com/book/zh-tw/%E9%96%8B%E5%A7%8B-%E5%88%9D%E6%AC%A1%E8%A8%AD%E5%AE%9AGit](http://git-scm.com/book/zh-tw/%E9%96%8B%E5%A7%8B-%E5%88%9D%E6%AC%A1%E8%A8%AD%E5%AE%9AGit)
2.ihower - Git 版本控制系統。[ihower - Git 版本控制系統](http://ihower.tw/git/intro.html)


