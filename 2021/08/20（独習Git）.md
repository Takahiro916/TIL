# TIL  

## 【独習Git】  

### 【Chapter 6　ファイルの追跡と更新】  
**`6.2 git addについて考える`**  
- リポジトリにコミットしたいファイルは`git add`を使わなければならない  

**`6.2.1 たとえ話によるステージングエリアの紹介`**
- 例えば、コードをこれから劇に登場する俳優だと考えると楽屋はディレクトリに相当する     
- 俳優は出演の準備を整え、出番が近づくとカーテンの裏で待機する。これがステージングエリアである。  
- 問題なければ俳優は演技を始める。それがコミットである。  

- 
**`6.2.2 変更をステージングエリアに追加する`**  

<演習>
```
% echo "echo \$a" >> math.sh
% ebho "b=2" >> math.sh
% bash math.sh
```
- `$a,b=2`の2行を追加、変数aの値を出力  

```
% git add math.sh
```
- 変更分をステージングエリアに配置  

**`6.2.3 ステージングエリアの更新`**  
<演習>
- 先ほど追加した`echo $a`は不要のため削除する    
```
% git status
``` 
- 出力結果  
```
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	modified:   math.sh

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   math.sh
```
- ファイルが2回変更(modifid)されたことくを示している  
- Changes to be committedはステージングされたことを意味している  
- Changes not staged for commitはコミット予定に入っていないという意味している  
- 片方はステージングエリアにあり、もう片方は作業ディレクトリにある！  

## 【寿司打】 ##  
**`10,000円コース【練習】`**
- 8,140円  

[![Image from Gyazo](https://i.gyazo.com/cbfb174e57567af3fd6580ba98934a1b.png)](https://gyazo.com/cbfb174e57567af3fd6580ba98934a1b)