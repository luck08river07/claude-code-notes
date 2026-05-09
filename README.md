# Claude Code 学習ノート

Claude Codeの学習過程を記録するブログサイトです。GitHub Pagesで公開できる構成になっています。

## ファイル構成

```
.
├── index.html                      # トップページ（記事一覧）
├── about.html                      # このサイトについて
├── assets/
│   └── style.css                   # 共通スタイル
├── posts/
│   └── claude-code-intro.html      # 記事：Claude Codeとは？
└── README.md                       # このファイル
```

## ローカルで確認する

`index.html` をダブルクリックしてブラウザで開けば、そのまま動作確認できます。

## GitHub Pagesで公開する手順

### 1. GitHubアカウントを用意

まだ持っていなければ <https://github.com/> でアカウントを作成します。

### 2. リポジトリを作成

GitHubにログインし、右上の「+」→「New repository」から新しいリポジトリを作ります。

- **Repository name**: 例 `claude-code-notes`
- **Public** を選択（GitHub Pagesの無料公開はPublicが必要）
- 「Create repository」をクリック

### 3. ファイルをアップロード

作成したリポジトリのページで「uploading an existing file」をクリックし、このフォルダの中身（`index.html` や `assets` フォルダなど）をすべてドラッグ＆ドロップしてアップロード、最後に「Commit changes」を押します。

> Gitに慣れている方は `git init` → `git remote add origin ...` → `git push` でも構いません。

### 4. GitHub Pagesを有効化

リポジトリの **Settings** タブを開き、左メニューの **Pages** を選びます。

- **Source**: 「Deploy from a branch」
- **Branch**: `main` / `/ (root)` を選択
- 「Save」をクリック

### 5. 公開URLを確認

数分待つと、Pagesの設定画面に公開URL（`https://<ユーザー名>.github.io/claude-code-notes/` のような形式）が表示されます。そのURLにアクセスすればサイトが公開されています。

## 新しい記事を追加する

1. `posts/` フォルダに新しいHTMLファイルを作成（既存の `claude-code-intro.html` をコピーして使うのが簡単です）
2. 記事のタイトル、日付、本文を書き換える
3. `index.html` の「最近の記事」リストに、新しい記事へのリンクを追加する
4. GitHubにアップロード（コミット＆プッシュ）すれば自動で反映されます

## デザインを変更したいとき

`assets/style.css` の冒頭にある `:root` の中の色（CSS変数）を変えると、サイト全体の雰囲気が変わります。

```css
:root {
  --color-link: #0969da;     /* リンクの色 */
  --color-accent: #cf5c2c;   /* アクセントカラー */
  /* ... */
}
```

## ライセンス

このサイトのコードは自由にコピー・改変して構いません。
