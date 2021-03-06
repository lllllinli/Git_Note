#Git安裝(在 Mac OS)#
<br>
## 1. Mac OS ##
內建 Git。
<br>
## 2. 設定 Git config ##
<br>
####必須設定三處：####
######1.'system'設定：######
檔案 **`/etc/gitconfig`**： 包含給該系統所有使用者的儲存庫使用的數值。 只要讀者傳遞 --system 參數給 git config，它就會讀取或者寫入參數到這個檔案。
<br>
######2.'使用者'設定：#######
檔案 **`~/.gitconfig`**： 給讀者自己的帳號使用。 傳遞 --global 參數給 git config，它就會讀取或者寫入參數到這個檔案。 
<br>
######3.'目前專案'設定：######
儲存庫內的設定檔，也就是 **`.git/config`**： 僅給所在的儲存庫使用。

######優先順序######

```````````
'目前專案' > '使用者' > 'system'
```````````
<br>
## 3.添加識別參數 ##

######全域 Goldel 設定：######

```````
$ git config --global user.name "使用者name"
$ git config --global user.email "使用者email"

```````

#####專案設定#####

```````
$ git config user.name "使用者name"
$ git config user.email "使用者email"

```````
*! 拿掉 `global`即可。*

#####指定編輯工具#####

``````
$ git config --global core.editor vim

``````
#####產生SSH Key#####

因為 Git 的伺服器大多使用 SSH public/private key 來做認證，請用以下步驟產生 SSH Key。

`````
ssh-keygen -t rsa -C "your_email@youremail.com"
cat ~/.ssh/id_rsa.pub
複製下來貼到 Github 帳號 -> Account Settings -> SSH Keys 裡
這樣在 Github 開專案，就可以 push 和 pull 下來了。

`````


####參考資料####
1.[http://git-scm.com/book/zh-tw/%E9%96%8B%E5%A7%8B-%E5%88%9D%E6%AC%A1%E8%A8%AD%E5%AE%9AGit](http://git-scm.com/book/zh-tw/%E9%96%8B%E5%A7%8B-%E5%88%9D%E6%AC%A1%E8%A8%AD%E5%AE%9AGit)
2.ihower - Git 版本控制系統。[ihower - Git 版本控制系統](http://ihower.tw/git/intro.html)


