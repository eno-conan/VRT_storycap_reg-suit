# Getting Started with Create React App
storybookのインストールコマンドは以下記事を参考にした。

https://www.asobou.co.jp/blog/web/chromatic-vrt

ライブラリのインストール

https://tech.uzabase.com/entry/2022/10/13/152134

スクリーンショットを取得するためのコマンド

https://blog.mmmcorp.co.jp/2022/08/29/storycap-reg-suit-codebuild/

以下コマンドを実行したときに成功した。
```
npx storycap --serverCmd "npx start-storybook -p 6006 --ci" http://localhost:6006
```
ただし、`package.json`に以下のように実装すると成功しない
```
storycap --serverCmd 'npx storybook -p 6006 --ci' http://localhost:6006
```
以下記事のコマンドで、実行できた。
https://blog.wadackel.me/2022/vrt-performance-optimize/
```
storycap http://localhost:6006 --serverCmd \"npx serve -l 6006 storybook-static\"
```
