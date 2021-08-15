# TIL  

## 【独習Git】  

### 【Chapter 4　リポジトリの作り方と使い方】  
**`4.3.1 git statusでリポジトリの状態をチェックする`**  

<演習>  
```
% cd
% cd buildtools
% git status
```
- カウントディレクトリ（現在のディレクトリ）は**pwd**で確認できる。  
- ｢コミットすべきものがない｣(nothing to commit)と表示される。
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

**`4.3.2 git addでファイルをリポジトリに追加する`**  
- Gitリポジトリに新しくファイルを入れたい時は**git add**を使う必要がある。  
- Gitが追跡管理できるのは｢追跡管理せよ｣と指示したファイルだけである。  

<演習>
```
% git add filexup.bat  
% git status  
```  
- 新しいファイルがあること(new file)と、それがコミットできること(to be committed)を表示。  

**`4.4 git commitでファイルをコミットする`**  
- ファイルをリポジトリにコミットすると｢タイムライン｣(timeline)が作られる。  
- **git commit**を使用し、ファイルをリポジトリにコミットする。  
- コミットの段階でタイムラインのエントリとしてリポジトリに保存される。  

<演習>  
```
% git commit -m "This is the first commit message"  
```

- メッセージは **-m** スイッチのあとに２重引用符で囲む。  


## 【寿司打】  
**`10,000円コース【練習】`**
- 7,640円  

[![Image from Gyazo](https://i.gyazo.com/c85ec8208491cbfe4835c283ae45fa99.png)](https://gyazo.com/c85ec8208491cbfe4835c283ae45fa99)