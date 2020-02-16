<template>
  <div>
    <h1>GraqhQLとは?</h1>
    <p>Facebookが2015年に開発した,Web API用のクエリ言語</p>
    <p>
      <strong>クエリ言語</strong>:クライアント側 <br /><strong
        >スキーマ言語</strong
      >:サーバー側<br />
      の2つからなる
    </p>
    <p>
      ひとつのエンドポイントに対してクライアントからクエリ言語を投げて,レスポンスをJSONで受け取る
    </p>
    <label>Query</label>
    <pre><code>{
  me {
    name
  }
}
</code></pre>
    <label>Response</label>
    <pre><code>{
  "me": {
    "name": "Luke Skywalker"
  }
}
</code></pre>
    <p>
      公式サイト<a target="_blank" href="https://graphql.org/"
        >https://graphql.org/</a
      >
    </p>
    <footer>
      <nuxt-link to="/">←back</nuxt-link>
      <nuxt-link to="/merit">Restful APIと比べての利点 →</nuxt-link>
    </footer>
  </div>
</template>
