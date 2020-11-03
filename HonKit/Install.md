---
description: HonKitでページをビルドするまで
---

# HonKitのセットアップとインストール

## ローカルインストール
HonKitはNode.jsで書かれているのでNode.jsのインストールが必要です。

```
$ npm install honkit --save-dev
# or
$ yarn add honkit --dev
```

## セットアップ
```
$ npx honkit init
```
### サブディレクトリを使用する場合
例えばGitGub Pagesでよくあるdocsフォルダを使用したい場合
```
$ npx honkit init ./docs
```
あわせて`book.json`で`root`を指定する必要がある
```book.json
{
    "root": "./docs"
}
```

### `SUMMARY.md`
HonKitはSUMMARY.mdファイルを使用して、本の章とサブ章の構造を定義します。このSUMMARY.mdファイルは、本の目次を生成するために使用されます
```
# Summary

* [Part I](part1/README.md)
    * [Writing is nice](part1/writing.md)
    * [HonKit is nice](part1/honkit.md)
* [Part II](part2/README.md)
    * [We love feedback](part2/feedback_please.md)
    * [Better tools for authors](part2/better_tools.md)
```

### `GLOSSARY.md`
注釈として表示する用語とそれぞれの定義を指定できます。これらの用語に基づいて、HonKitは自動的にインデックスを作成し、ページでそれらの用語を強調表示します。
```GLOSSARY.md
## Term
Definition for this term

## Another term
With it's definition, this can contain bold text
and all other kinds of inline markup ...
```

## プレビューする　
### ローカルでサーブする
```
yarn run honkit serve
```

### ローカルでビルドする
```
yarn run honkit build
```

## npm-run-scriptsとして定義
```package.json
  "scripts": {
    "build": "honkit build",
    "serve": "honkit serve"
  },
```
この構成の後、npm runコマンドを使用できます。
```
# Build 
npm run build
# Start to server
npm run serve
```