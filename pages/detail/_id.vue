<template>
  <div>
    <div v-if="!$apollo.loading">
      <img :src="pokemon.image" style="width:200px" />
      <div>
        <div>なまえ</div>
        {{ pokemon.name }}
      </div>
      <div>
        <div>タイプ</div>
        <ul>
          <li v-for="type in pokemon.types" :key="type">{{ type }}</li>
        </ul>
      </div>
      <div v-if="pokemon.evolutions">
        <div>しんか</div>
        <div v-for="evopoke in pokemon.evolutions" v-bind:key="evopoke.name">
          {{ evopoke.name }}
          <img :src="evopoke.image" style="widh:150px" />
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import getPokemon from '~/apollo/queries/getPokemon.gql'

export default {
  data() {
    return {
      id: this.$route.params.id,
      pokemon: {}
    }
  },
  apollo: {
    pokemon: {
      query: getPokemon,
      variables() {
        return {
          id: this.id
        }
      }
    }
  }
}
</script>
