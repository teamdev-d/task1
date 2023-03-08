# 初心者チーム開発 - 課題１

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
```
git branch <new-branch>
git switch <new-branch>
```
上記の作業を一回のコマンドで行っています。

### 2.3.2 - 手順
作業ブランチの名前は具体的な作業名にするのが通例です。
Blue Teamがindex.htmlに修正を加えるとします。

https://user-images.githubusercontent.com/91725975/223513350-8869b055-f773-4a9f-98d1-a5dc3bde2c8b.mov

## 2.4 - 追加機能作成
### 2.4.1 - 手順
Blue Teamがindex.htmlに挨拶を加えるとします。

https://user-images.githubusercontent.com/91725975/223513836-84a2952b-1295-40c7-9fe7-e69df6847909.mov

## 2.5 - ```git add .```で修正したファイルをgitに指示する（ステージング）

https://user-images.githubusercontent.com/91725975/223514736-1606586a-6f48-4603-a2a2-eed6716aa4c8.mov

## 2.6 - ```git commit -m "変更内容に関するメッセージ"```でステージングしたファイルの内容をgitに指示する

https://user-images.githubusercontent.com/91725975/223515739-5f4c8bf1-a412-4557-b9d8-dea16035108f.mov

## 2.7 - ```git push origin ブランチ名```でリモートリポジトリへ一連の作業内容を保存

(手順を示すためにvscodeのターミナルのスクショを載せる)

## 2.8 - developブランチへプルリクエストを作成する

(手順を示すためにgit hubのスクショを載せる)

## 2.9 - プルリクエストに対するレビューをしてもらう

(手順を示すためにgit hubのスクショを載せる)

## 2.10 - developブランチへマージする

(手順を示すためにgit hubのスクショを載せる)

---

## 2. Git の初期設定

### 2.1 - Organization を作成する

![Screenshot 2023-02-26 at 12 05 40](https://user-images.githubusercontent.com/45121253/221390035-79d95f3c-4474-4243-849e-334e650620fc.png)

**tips**
- Organization 内で複数のレポジトリを管理出来るため、上記では Quasar というレポジトリで Quasar のフレームワークの検証などを行っています。

<br />

### 2.2 - Repository を作成する

Organization 内で新しいレポジトリを作成し、下記のブランチ保護設定を ```develop``` と ```main``` に対して追加します。

![Screenshot 2023-02-26 at 12 25 42](https://user-images.githubusercontent.com/45121253/221390751-b60a42d3-f8b1-4cf6-9e95-2a76c6c189f3.png)

```Require a pull request before merging``` はパターンにマッチするブランチに対してマージする前に、プルリクエストを必須にする設定。

```Required number of approvals before merging``` はプルリクのレビューの approve の最低限の数を設定する（例:2に設定したら最低2人に承認を得る必要がある）

また、Github Actions などの CI を追加する場合、

![Screenshot 2023-02-26 at 12 35 24](https://user-images.githubusercontent.com/45121253/221390932-ab080dba-957d-4521-8a27-0d21b968a079.png)

---

## 3. 開発の流れ

### 3.1 - Issue を作って課題のタスク分けを行う
![Screenshot 2023-02-22 at 9 53 41](https://user-images.githubusercontent.com/45121253/220492780-2d96796f-e5bb-448f-a144-b70ee7b68fc0.png)

参考リンク
- [Issueの作成方法](https://docs.github.com/ja/issues/tracking-your-work-with-issues/creating-an-issue)
- [Issueで課題管理Assignee, Label, Project機能](https://style.potepan.com/articles/31077.html)
- [Markdown記法の書き方1](https://qiita.com/tbpgr/items/989c6badefff69377da7)
- [Markdown記法の書き方2](https://www.markdownguide.org/basic-syntax/)

<br />

### 3.2 - Issue に対する ```feature``` ブランチを ```develop``` から切る

```
git switch develop
git pull
git switch -c feature/#50_add_cpu
```

**tips**
- 最新の ```develop``` を pull してから ```feature``` ブランチを切りましょう
- ```feature``` ブランチ名を ```feature/#[Issue 番号]_XXXXXX``` に統一することでどの Issue に対するブランチなのかが明確になります

<br />

### 3.3 - ```feature``` ブランチで開発する

```
git add .
git status
git commit -m "#50 add random CPU"
```

**tips**
- コミット時のメッセージを ```#[Issue 番号] XXXXXX``` に統一することで Issue とコミットを紐付けられます

<br />

### 3.4 - 開発終了後、```develop``` へプルリクを作成する

```
git push origin feature/#50_add_cpu
```

![Screenshot 2023-02-22 at 9 52 23](https://user-images.githubusercontent.com/45121253/220492595-a6dafad3-aa0b-460b-9cc7-6355f7335ae3.png)

**tips**
- プルリクで今回の目的や実装の概要を書いてどのような変更を行なったのか説明しましょう
- ```closes #50``` などとプルリクに追記することでマージされた際 Issue を自動的に close することも出来ます

<br />

### 3.5 - 最低一人のメンバーにプルリクのレビューをしてもらう

![Screenshot 2023-02-26 at 11 54 24](https://user-images.githubusercontent.com/45121253/221389797-464e06b6-b13d-4572-9585-3c471f3a58f1.png)

```2.2``` で設定したプルリクに対する approve の最低個数や CI のチェックが満たされているかどうかを確認し、その場合マージします。

参考リンク
- [PullRequestで提案された変更をレビューする](https://docs.github.com/ja/pull-requests/collaborating-with-pull-requests/reviewing-changes-in-pull-requests/reviewing-proposed-changes-in-a-pull-request)
- [複数行へのレビュー](https://qiita.com/YumaInaura/items/65d59adbce322567ef14)
- [マージコンフリクトを解決する](https://docs.github.com/ja/pull-requests/collaborating-with-pull-requests/addressing-merge-conflicts/resolving-a-merge-conflict-on-github)
- [特定のpull requestをローカルに持ってくる](https://qiita.com/tarr1124/items/d807887418671adbc46f)
- [PullRequestでマージしたのを打ち消す](https://saikeblog.com/2020/03/09/github%E3%81%A7pull-request%E3%81%AE%E3%83%9E%E3%83%BC%E3%82%B8%E3%82%92%E6%89%93%E3%81%A1%E6%B6%88%E3%81%99%E6%96%B9%E6%B3%95/)
