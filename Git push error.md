# Git push error
> 2022/07/20


> 07/21 update
```bash=
git rm -r --cached .
git add .
git commit -m 'update .gitignore'
```

Using Gogs to host a git server, see this [instruction](https://ithelp.ithome.com.tw/articles/10210195)

---



```cmd=
>git push origin main
remote: error: Trace: 3faf7daa8a5fc7abbc91f74e47b35ee64801bf94f026284a8ae62953398b2a27
remote: error: See http://git.io/iEPt8g for more information.
remote: error: File data/mnist/resize/x_train.npy is 286.10 MB; this exceeds GitHub's file size limit of 100.00 MB
remote: error: GH001: Large files detected. You may want to try Git Large File Storage - https://git-lfs.github.com.
To https://github.com/Kuo-TingKai/TNNN.git
 ! [remote rejected] main -> main (pre-receive hook declined)
error: failed to push some refs to 'https://github.com/Kuo-TingKai/TNNN.git'
```

1. 我先試著在.gitignore裡面加了*.npy防止太大的檔案被add，但失敗了，但我找不出錯誤。我的.gitignore長這樣:
```.gitignore=
# 我在vscode裡面看到.npy檔呈灰色的 應該是被ignore了才對但結果沒有...
/data/mnist/origin/*.npy
/data/mnist/resize/*.npy
/history/history_npy/*.npy
/history/mpo/*
/img/
/model_weight/mpo
/src/relic/
```
folder tree長這樣:
![](https://i.imgur.com/fzIhYuF.png)![](https://i.imgur.com/zgYn2mO.png)


3. 我又用了[git-lfs](https://haway.30cm.gg/git-lfs/) ，但應該沒啥用