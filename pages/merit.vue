<template>
  <div>
    <h1>Restful APIと比べての利点</h1>
    <h2><small>一回のリクエストで必要なリソースが取得できる</small></h2>
    <p>
      Restful
      APIだと、必要なリソースをすべて取得するのに複数回APIを投げる必要がある
      <br />
      QeaphQLなら1回リクエストを投げるだけで済む
    </p>
    <label>例:Query</label>
    <pre><code>{
  me {
    id
  },
  user {
    name
  },
  schedule{
    date
    status
  }
}
</code></pre>
    <h2><small>必要なものを必要な分だけ</small></h2>
    <p>
      クエリなので、取得したいものをクライアント側で柔軟に指定できる
    </p>
    <h2>使うと良さそうなシーン</h2>
    <ul>
      <li>通信量の制限がシビアな、モバイルネットワークでの利用</li>
      <li>フロントとバックエンドの距離がある現場や公開APIなど</li>
    </ul>
    <footer>
      <nuxt-link to="/whatgraphql">←back</nuxt-link>
      <nuxt-link to="/sampleserver">つかってみよう! →</nuxt-link>
    </footer>
  </div>
</template>
