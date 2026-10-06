# 薬歴 ― くすりの歴史 ―

薬草からmRNAワクチンまで。くすりの発展の歴史をたどるシミュレーションゲーム。

## ファイル構成

```
index.html              ゲーム本体（1ファイルで完結）
manifest.webmanifest    ホーム画面追加（PWA）用の設定
assets/
  icon-1024.png         アイコンのマスター画像（1024×1024）
  icon-512.png          PWA / Android（512×512）
  icon-192.png          PWA / Android（192×192）
  apple-touch-icon.png  iPhone / iPad ホーム画面（180×180）
  favicon-32.png        ブラウザのタブ（32×32）
  ogp.png               SNS共有画像（1200×630）
```

フォルダごと GitHub Pages / Cloudflare Pages に置けば動きます。パスはすべて相対パスなので、サブディレクトリに置いても壊れません。

## 公開前に1か所だけ書き換える

`index.html` の `【公開URL】` を、公開先のURL（末尾の `/` なし）に置き換えてください。2か所あります。

- `og:image`
- `twitter:image`

例：`【公開URL】/assets/ogp.png` → `https://example.pages.dev/assets/ogp.png`

SNSの共有画像は、絶対URLでないと表示されません。あわせて、コメントアウトしてある `og:url` も有効にしてください。

## 画像の差し替え

`assets/` の画像は暫定版です。正式な画像ができたら、同じファイル名・同じサイズで上書きしてください。HTMLの変更は要りません。

## セーブ

セーブはブラウザの localStorage（キー `pharma-3layer-v2`）に保存されます。ゲーム名を変えてもキーは変えていないので、以前の版のセーブはそのまま引き継がれます（同じアドレスで公開している場合）。
