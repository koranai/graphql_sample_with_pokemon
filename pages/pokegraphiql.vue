<template>
  <div>
    <h1>クエリを実際に発行してみよう</h1>
    <h3><small>クエリをさわってみる</small></h3>
    <span>Graph<em>i</em>QL</span
    >というブラウザからGraphQLをつかえるツールを使用してあそぶ
    <p>
      <a target="_blank" href="https://graphql-pokemon.now.sh/"
        >https://graphql-pokemon.now.sh/</a
      >
    </p>
    <h3><small>クライアントに組み込んでみる</small></h3>
    <p>
      <nuxt-link target="_blank" to="/sample"
        >Nuxt.jsからPokemon-graphQLを呼ぶサンプル</nuxt-link
      >
    </p>
    <footer>
      <nuxt-link to="/sampleserver">←back</nuxt-link>
      <nuxt-link to="/end">おわり →</nuxt-link>
    </footer>
  </div>
</template>
