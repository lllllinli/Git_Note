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
/*
* 檔案已經 commit ，刪除檔案．
*/

$git reset HEAD <file>...

`````
##4.Git 刪除已經commit的檔案 ##

`````
/*
* 檔案已經 commit ，刪除檔案．
*/

$git rm filename

`````
##5.Git 移動或更名已經commit的檔案 ##

`````
/*
* 檔案已經 commit ，更名檔案．

*/

$git rm filename newFilename

`````
##6.Git Commit的幾種指令 ##

`````
$git commit
$git commit -m 'commit message'
$git commit -a -m 'commit -message' # 將所有修改過得檔案都 commit, 但是 新增的檔案 還是得要先 add.
$git commit -a -v # -v 可以看到檔案哪些內容有被更改, -a 把所有修改的檔案都 commit

`````

##5.把commit上傳到網路空間 ##

`````
/*
* 檔案已經 commit ，上傳到網路空間．

*/

$git push

`````
##5.更新網路空間的 master repository ##

`````
/*
* 檔案已經 commit ，上傳到網路空間．

*/

$git pull

`````
##6.建立  .gitignore 檔##

####(1).建立####

`````
$cd 專案目錄下
$touch .gitignore

`````
####(1).編寫方式####

#####注意-#####

`````
//空白列或者以#開頭的列會被忽略。
//可使用標準的Glob pattern。
//可以/結尾，代表是目錄。
//可使用!符號將特徵反過來使用。

`````
#####範例-#####

`````
# 註解，會被忽略。
# 不要追蹤檔名為 .a 結尾的檔案
*.a
# 但是要追蹤 lib.a，即使上方已指定忽略所有的 .a 檔案
!lib.a
# 只忽略根目錄下的 TODO 檔案。 不包含子目錄下的 TODO
/TODO
# 忽略build/目錄下所有檔案
build/
# 忽略doc/notes.txt但不包含doc/server/arch.txt
doc/*.txt
# ignore all .txt files in the doc/ directory
doc/**/*.txt

`````
#####常用忽略commit檔案設定#####

`````
tmp/*
log/*
你個人環境的設定檔(例如你偏愛的編輯器設定檔)
可以自動產生的檔案
build/* 等 compile 之後的檔案
.DS_Store
Thumbs.rb

`````

####參考資料####
1.git-scm。[http://git-scm.com/book/zh-tw/%E9%96%8B%E5%A7%8B-%E5%88%9D%E6%AC%A1%E8%A8%AD%E5%AE%9AGit](http://git-scm.com/book/zh-tw/%E9%96%8B%E5%A7%8B-%E5%88%9D%E6%AC%A1%E8%A8%AD%E5%AE%9AGit)
2.ihower - Git 版本控制系統。[ihower - Git 版本控制系統](http://ihower.tw/git/intro.html)


