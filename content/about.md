+++
title = "あばうと"
date = 2022-01-01T00:00:00+09:00
+++

あばうとのページ。

![サンプル画像](../images/1920x1080.jpg)

固定ページと記事投稿は、相対リンクの階層が異なるので、記述に注意する。


## 環境

- x230（Lenovo ThinkPad）
- LinuxMint 20.2


## 補足

サクッと使う個人的な用途で小規模を想定。

blogフォルダへ投稿を詰め込んで、タグで仕分けるイメージ。

HUGOで個人的に使うシンプルなテーマ。

久しぶりすぎて、およそ5時間くらいで作ったので、大雑把にやっつけです。（2022-01-16）


## 基本的な仕様

- hugo v0.92.0
- pure.css
- config.toml
	- baseURL（最後のスラッシュ有り）
- toml形式を採用（記事投稿のデフォルト設定）
- カテゴリー無し
- タグ（tags）有効
- 投稿のタグ付けは日本語を使わないようにする（翻訳・英訳）
- デフォルトは、10件ごとのページ送り
	- config.toml,Paginate = 10
- 任意のページ送り:5件ごとで設定
	- hugo-do-simple/layouts/_default/taxonomy.html,.Paginator 5
- 固定ページ（デフォルト:日付表示なし）
	- hugo-do-simple/layouts/_default/single.html,コメントアウト

<p>基本的なファイル一式はGitHubに置いておきます。</p>
<ul>
<li><a href="https://github.com/hikagestyle/hugo-do-simple" target="_blank" rel="nofollow noopener noreferrer">hugo-do-simple</a></li>
</ul>


## 注意点と覚え書き

- 記事に「日本語のタグ付け」は避けたほうが良い。（ビルド生成される日本語フォルダは、相性の悪いサーバーがある）
- タグの並び順は、アルファベット順が無難。（terms.html,Alphabetical,<a href="https://gohugo.io/templates/taxonomy-templates/" target="_blank" rel="nofollow noopener noreferrer">Taxonomy Templates</a>）
- 多機能なので、シンプルに記事投稿へ集中するほうが負担は少ない。
- config.tomlは、記述のルールや順番がある。（<a href="https://gohugo.io/getting-started/configuration/" target="_blank" rel="nofollow noopener noreferrer">Configure Hugo</a>）


## ビルドまでの流れ

- config.tomlの編集
	- baseURL(最後のスラッシュ有り)
	- title
	- description
- templatesを必要に応じて編集
	- hugo-do-simple/layouts/partial/_analytics.html
	- hugo-do-simple/layouts/partial/_sidebar.html
	- hugo-do-simple/layouts/index.html
- 記事の作成
	- mdファイル(content/blog)
- ローカルチェック
	- hugo server
	- hugo server -D
- ビルド
	- hugo
	- hugo -D
- publicフォルダが生成される

