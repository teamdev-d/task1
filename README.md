# 初心者チーム開発 - 課題１

## 前提条件

使用するリポジトリをクローンできている状態。

クローンできていない場合はコチラの動画を参考にしてください。

1.リポジトリのURLを取得
2.vscodeの「Gitリポジトリのクローン」を使用

https://user-images.githubusercontent.com/91725975/223794835-6eec0ad7-0240-4e40-a0c6-4fa163a67d28.mov

## 概要

初心者チーム開発で使用するgitをハンズオンで解説します、主な流れとしては:
1. Issueを作って自分のタスクを登録する
2. developブランチにて```git pull```を実行
3. ```git switch -c ブランチ名```で追加機能用のブランチを作成、移動
4. 追加機能作成
5. ```git add .```で修正したファイルをgitに指示する（ステージング）
6. ```git commit -m "変更内容に関するメッセージ"```でステージングしたファイルの内容をgitに指示する
7. ```git push origin ブランチ名```でリモートリポジトリへ一連の作業内容を保存
8. developブランチへプルリクエストを作成する
9. プルリクエストに対するレビューをしてもらう
10. developブランチへマージする

---

## 1. スタートとゴール

概要にある作業を全員が行い下記の成果物を作成することが目標。

### スタート

<img width="1440" alt="スクリーンショット 2023-03-07 2 14 39" src="https://user-images.githubusercontent.com/91725975/223183271-8409cbd3-5eb0-469f-8227-436f5bb9bf94.png">

### ゴール

<img width="1440" alt="スクリーンショット 2023-03-07 2 14 30" src="https://user-images.githubusercontent.com/91725975/223183351-b001ba55-5b61-47a5-9293-100f5b94a8ea.png">


---

## 2. 開発の流れ

### 重要:ここから本格的な作業に移ります、以下の具体例では、Red Teamが作業を終え、Blue Teamが作業を開始することを想定しています。

## 2.1 - Issueを作って自分のタスクを登録する

### 2.1.1 - Isuueとは
Isuueとは開発メンバー間で共有が必要な事項をスレッド形式で立てられる機能です。

<img width="1439" alt="スクリーンショット 2023-03-07 1 39 37" src="https://user-images.githubusercontent.com/91725975/223174776-b120fe05-cdb1-4ea8-8c2e-78e7a0ba8c77.png">

Issueの詳しい説明はコチラ（ドキュメントのリンク）
参考リンク
- [Issueの作成方法](https://docs.github.com/ja/issues/tracking-your-work-with-issues/creating-an-issue)
- [Issueで課題管理Assignee, Label, Project機能](https://style.potepan.com/articles/31077.html)
- [Markdown記法の書き方1](https://qiita.com/tbpgr/items/989c6badefff69377da7)
- [Markdown記法の書き方2](https://www.markdownguide.org/basic-syntax/)

### 2.1.2 - 手順

### 作成の手順　　

https://user-images.githubusercontent.com/91725975/223501847-d34df101-0302-4abf-96b4-3c710594229d.mov

### closeの手順

https://user-images.githubusercontent.com/91725975/223501285-1902a42e-7004-4429-8cb4-8f3883937899.mov



## 2.2 - developブランチにて```git pull```を実行

### 2.2.1 - ```git pull``` の説明と具体例
git pullとは、リモートリポジトリから最新の状態をローカルリポジトリに反映するコマンドです。

例えば、Red Teamが「Hello Red Team」をindex.htmlに追加し、developブランチにマージしたとします。
そうするとRed Teamとそれ以外のチームで差異が生じます。

#### Red Teamのブラウザ
<img width="1440" alt="Hello Rec and Red" src="https://user-images.githubusercontent.com/91725975/223505886-1461c4c5-13a1-415d-a431-cf853787a927.png">

#### それ以外のチームのブラウザ
<img width="1440" alt="Hello Recursion" src="https://user-images.githubusercontent.com/91725975/223505998-9767e7f9-c1c0-45ca-92fd-a99aeb29d0c6.png">

### 2.2.2 - 手順

※注意developブランチにいない場合```git switch develop```でdevelopブランチに戻る必要があります。

https://user-images.githubusercontent.com/91725975/223508120-1ffacf47-33d5-4c71-ac80-662c43547d94.mov

## 2.3 - ```git switch -c ブランチ名```で追加機能用のブランチを作成、移動

### 2.3.1 - ```git switch -c ブランチ名```の説明
```-c```はgitのコマンドに用意されたオプションであり、createのcです。このオプションでブランチの作成を行っています。
要するに下記の作業を一回のコマンドで行っています。
```
git branch <new-branch>
git switch <new-branch>
```

### 2.3.2 - 手順
作業ブランチの名前は具体的な作業名にするのが通例です。
Blue Teamがindex.htmlに修正を加えるとします。

https://user-images.githubusercontent.com/91725975/223513350-8869b055-f773-4a9f-98d1-a5dc3bde2c8b.mov

## 2.4 - 追加機能作成
### 2.4.1 - 手順
Blue Teamがindex.htmlに挨拶を加えるとします。

https://user-images.githubusercontent.com/91725975/223513836-84a2952b-1295-40c7-9fe7-e69df6847909.mov

## 2.5 - ```git add .```で修正したファイルをgitに指示する（ステージング)
### 2.5.1 - ```git add```の説明
git addコマンドは、Gitのステージングエリアに変更を追加するために使用されます。言い換えれば、次のコミットにどの変更を含めたいかをGitに伝えるために使用されます。


```git add path/to/file```で特定のファイルをステージングエリアに追加できます。


```git add .```でディレクトリ配下の全てのファイルの変更をステージングエリアに追加できます。

### 2.5.2 - 手順

```git add .```を使います。

https://user-images.githubusercontent.com/91725975/223514736-1606586a-6f48-4603-a2a2-eed6716aa4c8.mov

## 2.6 - ```git commit -m "変更内容に関するメッセージ"```でステージングしたファイルの内容をgitに指示する


### 2.6.1 - ```git commit -m "変更内容に関するメッセージ"```の説明
git commitコマンドは、ローカルリポジトリへの変更を記録するためにGitで使用されます。言い換えれば、2.5で使用したgit addコマンドでステージングしたファイルの内容を記録しているということです。

```-m```オプションを使用すると、行った変更を説明するメッセージを含めることができます。

### 2.6.2 - 手順

https://user-images.githubusercontent.com/91725975/223515739-5f4c8bf1-a412-4557-b9d8-dea16035108f.mov

## 2.7 - ```git push origin ブランチ名```でリモートリポジトリへ一連の作業内容を保存

### 2.7.1 - ```git push origin ブランチ名```の説明
git pushコマンドは、Gitリポジトリに加えられたローカルの変更をリモートリポジトリにアップロードするために使用されます。言い換えれば、2.5、2.6で行った作業をローカルからリモートリポジトリに反映させています。


```origin```とはリモートリポジトリのアクセス先に対してGitがデフォルトでつける名前です。言い換えれば、みなさんがリポジトリをクローンするために使ったURLの内容を```origin```としています。


### 2.7.2 - 手順


https://user-images.githubusercontent.com/91725975/223714422-db6b84e7-6911-456d-8b2f-f4ec7bf905e2.mov



## 2.8 - developブランチへプルリクエストを作成する

(手順を示すためにgit hubのスクショを載せる)

## 2.9 - プルリクエストに対するレビューをしてもらう

(手順を示すためにgit hubのスクショを載せる)

## 2.10 - developブランチへマージする

(手順を示すためにgit hubのスクショを載せる)

---
