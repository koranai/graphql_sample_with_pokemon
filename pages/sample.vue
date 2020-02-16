<template>
  <div>
    <div class="boxcontainer">
      <div v-for="poke in pokemons" v-bind:key="poke.name" class="box">
        <nuxt-link v-bind:to="/detail/ + poke.id">
          <img :src="poke.image" />
          <label>{{ poke.name }}</label>
        </nuxt-link>
      </div>
    </div>
  </div>
</template>

<script>
import getList from '~/apollo/queries/getList.gql'

export default {
  components: {},
  data() {
    return {
      pokemons: {}
    }
  },
  apollo: {
    pokemons: {
      query: getList
    }
  }
}
</script>

<style scoped>
.boxcontainer {
  display: flex;
  flex-wrap: wrap;
}
.box {
  width: 50%;
  position: relative;
}
.box img {
  max-width: 100%;
  height: 170px;
}
.box label {
  padding: 2px;
  position: absolute;
  background: #bfbfbfbf;
  color: #ffffff;
  left: 0;
  bottom: 0;
  width: calc(100% - 4px);
}
</style>
