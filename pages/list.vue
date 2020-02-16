<template>
  <div class="container">
    <div>
      <div v-for="poke in pokemons" v-bind:key="poke.name">
        <label>{{ poke.name }}</label>
        <img :src="poke.image" />
      </div>
      <!-- <logo />
      <h1 class="title">pokemonviewr</h1>
      <h2 class="subtitle">samole app for learn to graphql</h2>
      <div class="links">
        <a href="https://nuxtjs.org/" target="_blank" class="button--green"
          >Documentation</a
        >
        <a
          href="https://github.com/nuxt/nuxt.js"
          target="_blank"
          class="button--grey"
          >GitHub</a
        >
      </div> -->
    </div>
    {{ pokemon }}
    {{ pokemons }}
  </div>
</template>

<script>
// import Logo from '~/components/Logo.vue'
// import getPokemon from '~/apollo/queries/getPokemon.gql'
import getList from '~/apollo/queries/getList.gql'

export default {
  components: {
    // Logo
  },
  data() {
    return {
      pokemon: {},
      pokemons: {}
    }
  },
  apollo: {
    // pokemon: {
    //   query: getFushigidane,
    //   variables: { name: 'Bulbasaur' }
    // }
    pokemons: {
      query: getList
    }
  }
}
</script>

<style>
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
</style>
