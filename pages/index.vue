<template>
  <div>
    <div v-if="!$apollo.loading" style="margin-top:40px;">
      <center>
        <img :src="pokemon.image" style="width:240px;" />
        <h1>GraphQLさわってみたよ！</h1>
        <p>2020/2/21 社内勉強会用</p>
      </center>
      <center style="font-size:2em;">
        <nuxt-link to="/about">→ Start!</nuxt-link>
      </center>
    </div>
  </div>
</template>

<script>
import getPokemon from '~/apollo/queries/getPokemon.gql'

export default {
  components: {},
  data() {
    return {
      pokemon: {}
    }
  },
  apollo: {
    pokemon: {
      query: getPokemon,
      variables: { id: 'UG9rZW1vbjowNTQ=' }
    }
  }
}
</script>

<style scoped>
a {
  font-size: 2em;
}
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
center {
  margin-top: 40px;
}
</style>
