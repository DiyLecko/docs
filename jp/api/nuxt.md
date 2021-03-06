---
title: "API: Nuxt(options)"
description: Nuxt.js はプログラム上で、ミドルウェアとして使うことができます。そうすることでウェブアプリケーションをレンダリングする独自のサーバーを自由に作ることができます。
---

<!-- title: "API: Nuxt(options)" -->
<!-- description: You can use nuxt.js programmatically to use it as a middleware giving you the freedom of creating your own server for rendering your web applications. -->

<!-- # Using Nuxt.js Programmatically -->

# Nuxt.js をプログラムで使う

<!-- You might want to use your own server with your middleware and your API. That's why you can use Nuxt.js programmatically. -->

ミドルウェアや API と合わせて独自サーバーを使いたいときがあるかもしれません。そのため、Nuxt.js はプログラムで使うことができるようにしています。

<!-- Nuxt.js is built on the top of ES2015, which makes the code more enjoyable and cleaner to read. It doesn't make use of any transpilers and depends upon Core V8 implemented features. For these reasons, Nuxt.js targets Node.js `4.0` or higher. -->

Nuxt.js は ES2015 以上でビルドされます。ES2015 はコーディングをより楽しいものし、より読みやすくしてくれますよね。また、Nuxt.js はトランスパイラを利用せず、また V8 エンジンで実装された機能に依存しません。このような理由から Nuxt.js は Node.js `4.0` 以上をターゲットにしています。

<!-- You can require Nuxt.js like this: -->

Nuxt.js をこのように require できます:

```js
const Nuxt = require('nuxt')
```

## Nuxt(options)

<!-- To see the list of options to give to Nuxt.js, see the configuration section. -->

Nuxt.js に渡すことができるオプション一覧を見るには、設定のセクションを参照してください。

<!-- ```js -->
<!-- const options = {} -->

<!-- const nuxt = new Nuxt(options) -->
<!-- nuxt.build() -->
<!-- .then(() => { -->
<!--   // We can use nuxt.render(req, res) or nuxt.renderRoute(route, context) -->
<!-- }) -->
<!-- ``` -->

```js
const options = {}

const nuxt = new Nuxt(options)
nuxt.build()
.then(() => {
  // nuxt.render(req, res) あるいは nuxt.renderRoute(route, context) を使うことができます
})
```

<!-- You can take a look at the [nuxt-express](https://github.com/nuxt/express) and [adonuxt](https://github.com/nuxt/adonuxt) starters to start quickly. -->

手っ取り早く始めるために [nuxt-express](https://github.com/nuxt/express) や [adonuxt](https://github.com/nuxt/adonuxt) スターターを参照できます。

### ログを使ってデバッグする

<!-- If you want to display nuxt.js logs, you can add to the top of your file: -->

Nuxt.js のログを表示したいときはファイルのトップに次のコードを追加してください:

```js
process.env.DEBUG = 'nuxt:*'
```
