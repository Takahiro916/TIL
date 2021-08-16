# TIL  

## 【独習Git】  

### 【Chapter 4　リポジトリの作り方と使い方】  
**`4.5 git logとgit ls-filesで、リポジトリを調べる`**  

<演習>  
```
% git status
% git log
```
- 第1のコマンドは｢作業ディレクトリがクリーンな状態であり、コミットするべきものが存在しない｣("nothing to commit, working tree clean")と表示。  
- 第2のコマンドはログを表示。
- ファイルの追跡(track)を開始する方法を教えてくれる。(use git add to track)  
- Gitが追跡できるファイルを1つ作成する。  

<演習>  
```
% cd  
% cd buildtools
% echo -n contents  
% echo -n contents > filexup.bat  
% git status  
```
- buildtoolsディレクトリに移動し、echoコマンドにてファイルを1つ作成。  
- Gitが作業ディレクトリ内に新しいファイルを検出する。  
- そのファイルを｢追跡していない｣(untracked)と指摘している。  
- ｢git addを使えば追跡できます｣(use "git add" to track)と提案している。

```
% git ls-files
```
- リポジトリに入っているファイルのリストを確認。  

**`4.6 課題`**  
1. "does not have any commits yet"  
ディレクトリが作成されただけで、なにもコミットされていないため。  

2. 
```
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
	new file:   file.txt

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   file.txt
```

3. 
```
 Changes not staged for commit:
 (use "git add <file>..." to  update what will be committed)
 (use "git restore <file>..." to discard changes in working directory)
 modified:   file.txt
 ```

## 【寿司打】 ##  
**`10,000円コース【練習】`**
- 7,640円  

[![Image from Gyazo](https://i.gyazo.com/c4580dd7dd502b10b021a5816ccf80fb.png)](https://gyazo.com/c4580dd7dd502b10b021a5816ccf80fb)  

## 【今日の振り返り】  
- 5時半朝礼の当番だったが寝坊してしまった（6時起床）・・・。  
- 自己申告書提出。挑戦してみたいことを思いのままに記載！  
