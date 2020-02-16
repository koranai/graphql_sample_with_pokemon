<template>
  <div>
    <h1>つかってみよう!</h1>
    <h1><small>公開されているGraqhQLサーバー</small></h1>
    <label>公式API系</label>
    <ul>
      <li>
        <a
          target="_blank"
          href="https://developer.github.com/v4/guides/forming-calls/#authenticating-with-graphql"
        >
          Github</a
        >
      </li>
      <li>
        <a
          target="_blank"
          href="https://github.com/kibela/kibela-api-v1-document"
          >Kibela</a
        >
      </li>
    </ul>
    <label>非公式API系</label>
    <ul>
      <li>
        <a target="_blank" href="https://github.com/graphql/swapi-graphql">
          swapi-graphql：Star warsの登場人物等が検索できる</a
        ><br />graphqlのチュートリアルサイトのスキーマが実装されてる(graphqlのprojectなので半公式？)
      </li>
      <li>
        <a target="_blank" href="https://github.com/lucasbento/graphql-pokemon"
          >GraphQL Pokémon: ポケモン初代(151匹)が検索できる</a
        ><br />
        今回はこれをつかってあそぶ!
      </li>
    </ul>
    <footer>
      <nuxt-link to="/merit">←back</nuxt-link>
      <nuxt-link to="/pokegraphiql">クエリを発行してみよう →</nuxt-link>
    </footer>
  </div>
</template>
