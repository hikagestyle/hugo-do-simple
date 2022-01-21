# まえがき

HUGO（静的サイトジェネレーター）のテーマ。

個人的なファイル一式。

修正や加工ほか、ご利用は自己責任で。


## 環境

- x230(Lenovo ThinkPad)
- LinuxMint 20.2


## 補足

サクッと使う個人的な用途で小規模を想定。

blogフォルダへ投稿を詰め込んで、タグで仕分けるイメージ。

HUGOで個人的に使うシンプルなテーマ。

久しぶりすぎて、およそ5時間くらいで作ったので、大雑把にやっつけです。（2022-01-16）


### 2022-01-22（修正）

- 微調整
	- themes/hugo-do-simple/static/css/style.css

### 2022-01-19（修正）

- 微調整
	- themes/hugo-do-simple
	- content/about.md

### 2022-01-17（変更）

- 微調整
	- themes/hugo-do-simple
	- content/blog


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


## 完成イメージ

デモサイト: <a href="https://hugo-do-simple.netlify.app/" target="_blank">https://hugo-do-simple.netlify.app/</a>


## 公式サイト

- [HUGO](https://gohugo.io/)
- [Pure](https://purecss.io/)

